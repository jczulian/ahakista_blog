---
layout: post
title:  "How to delete tags in git"
date:   2013-10-29
categories: 
---

Deleting tags in git is an easy task. The following command will do it

{% highlight bash %}
git tag -d <tag_name>
{% endhighlight %}

This however only delete the tag reference existing in you local repository. If the tag has been pushed to other repositories these one won't get affected by the previous command. As usual with git when you want to share your references (branch, tag) you need to push to the repository with which you want to share them.

The trick when you are deleting a reference is that you don't want to push something to another repository but rather push nothing. In git there is way to say that you want to push nothing. At first it seems rather obscure syntax but it actually all make sense with a little explanation.

So here is the way to delete a tag on a remote repository:

{% highlight bash %}
git push origin :<tag_name>
{% endhighlight %}

This is rather weird syntax. The first part is normal, you are saying that you want to push to the origin repository. But the ':<tag_name>' part looks strange.

In order to understand it lets consider the normal way to push from a local reference to a remote one. In other words how you would push a local branch to a remote branch:

{% highlight bash %}
git push origin refs/heads/master:refs/heads/master
{% endhighlight %}

The 'refs/heads/master' is actually a file on your file system inside the .git folder of the current repository. Go ahead and have a look at what is in the .git/refs/heads/master folder. You might not recognize what this is, but the content of this file is simply the hash of a commit. So basically all your refs are just in the end file in your .git folder whose content is a simple sha1 of the commit it points to.

Now the next bit to understand is the 'refs/heads/master:refs/heads/master'. This means simply \<from>:\<to>. With it you are saying that you want to push the local commit referenced by the first part (before the ':') to the remote repository under the reference designated by the second part (logically after the ':').

With this knowledge it has become easier to understand the syntax used to delete a tag (or any other reference). By giving no <from> part you are simply saying _copy nothing_ to this remote something. The net effect is that the remote reference will point to nothing (no commit) hence deleting it.

It exist since some version of git a more user friendly syntax to perform deletions:

{% highlight bash %}
git push --delete origin tagname
{% endhighlight %}

This is strictly equivalent to the previous syntax. It might convey the intent in a more obvious way but I somehow like the original syntax as it is really explicit about what is happening underneath the surface.

To sum it up we can say that pushing a branch, tag, or other refs to a remote repository involves specifying "push where, what source, what destination?"

{% highlight bash %}
git push where-to-push source-ref:destination-ref
{% endhighlight %}

Normally you never have to give a full path to your reference. Git knows about the default path and so you can shorten your reference by just giving their name, like so:

{% highlight bash %}
git push origin master:master
{% endhighlight %}

You can do even shorter if you git's configuration knows about the tracking branch of your local branch. If such is the case then you only have to give the branch name you want to push. Git will look at the configuration and know automatically where he should put the branch to.


{% highlight bash %}
git push origin master
{% endhighlight %}
