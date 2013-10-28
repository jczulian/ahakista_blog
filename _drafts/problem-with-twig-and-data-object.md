---
layout: post
title:  "The problem with Twig and data Object "
date:   2013-10-22
categories: 
---

Sonata adming offers a base_list.html.twig template
defined blocks can be over written
claim is that template and logic is separated
if you pass object to your template the logic is not any more separated
You have to know how your object looks like and behave in order to navigate the object graph
You cannot replace object in the object graph easily with simple data (like an array) because you have to recreate the whole objects hierachy and graph 

Result: you copy your original temple fully and tell it to read data from somewhere else, so much for code reuse.

I actually thought afterward that you could over write the template part of interest and just read data from somewhere else of my choosing. Unfortunately the datagrid object is just use every where in the template. No luck, no reuse.

The data sent to a template must be without any logic if you want to have reusable template and separate definitely template and logic.

The contract between the controller and the template should only be about where the data is and where to find it. Xml and xslt separation in Okapi were quite good at keeping thing separated and not having templates calling in the business object. 

You cannot extend your data with more data. I want for example to add for every license the list of courses they have been used for. I can't add this list to the license object easily. Well in that case I guess I can, the data is already there and would just have to call the getCourses() method on each license. But the point remains that if I want to attache any kind of extra data to the element to be render I cannot do it, unless the object already permit it. Otherwise you are screwed up.
