---
layout: post
title:  "Php's preg_grep function has a strange behavior"
date:   2013-11-02
tags: [php]
categories: 
---

The other day at work I had to do some task that uses php's regular expression functions. And then I stumble upon, what we could qualify, as a strange behavior of the preg_grep function.

This function takes as first argument a string containing a regular expression and as second argument an array of string. It also takes an optional third argument that allows one to get obtain the non matching strings instead of the matching ones.

I was actually expecting the function to return me a freshly created new array with only the matching strings. But it doesn't do exactly that. 

The documentation states that the function "Return array entries that match the pattern". What it doesnt tell you is that it will return the same array with the non-matching entries removed from the array.

Arrays in PHP are of two "types". They can be integer indexed array or string indexed array, what it is called an hash map or dictionnary in many other languages. But in PHP this two kind are put into one and the same syntax is used to create and use them. In fact an integer indexed array is somehow an hashmap having for keys the integer values.

Now the funny thing with preg_grep is that, as said earlier, doesn't build a new array with the matching strings. No, instead it takes the original array removes the non-matching strings and give you back the array. What is extremely weird and puzzling is that if you ask for the first element of the resulting array you might get nothing even though you are sure you must have had some matches.

What is happening is the following. Let's pretend we have passed as argument this array:

{% highlight php %}
$array = array('Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday');
{% endhighlight %}

and we perform the following preg_grep function on it:

{% highlight php %}
matching_days = preg_grep('/es/', $array);
{% endhighlight %}

We would expect to receive in return an array containing only the week days having an 'es' in their names, and so we might be tempted to use like this:

{% highlight php %}
$first_matching_day = $matching_days[0];
{% endhighlight %}

Unfortunately this won't work at all and you will receive an error message from php telling you that there is actually nothing at index key '0'.

If you var_dump the said array you will see that php didn't lie to you and that preg_grep is strange:

{% highlight php %}
array(2) {
  [1]=>
  string(7) "Tuesday"
  [2]=>
  string(9) "Wednesday"
}
{% endhighlight %}

There is nothing at indexe 0. The function has kept the string indexed as they were in the original array: "Tuesday" is at index 1 and "Wednesday" is at index 2. 

This is rather confusing I think. Although I understand why PHP does that I really think that this is not a great behavior.

The reason why the resulting array keeps the original key indexes as to do with the fact that, as we have said at the begining, PHP's array are of two kinds: array and hashmap.And in the case you give to the preg_grep function an array that is in fact a real hashmap then you really want the function to maintain the original keys and the value the map too associated. The thing is that no function has the power to tell if your array is actually a "real array" or an hashmap. And that's a bummer, especially in this case.
