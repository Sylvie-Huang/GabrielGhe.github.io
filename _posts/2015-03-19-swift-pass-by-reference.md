---
layout: post
title: "Swift: Pass By Reference"
description: "In some cases, you would like to pass a variable by reference. In Swift, we use the `inout` and the `&` keys.
Here's an example of a generic swap."
category: swift
tags: [ios, inout, reference]
---
{% include JB/setup %}

<!-- Overview -->
<h3>Overview</h3>

In some cases, you would like to pass a variable by reference. In Swift, we use the `inout` and the `&` keys.
Here's an example of a generic swap.

<!-- Code _______________________________________-->
{% highlight swift linenos=table  %}
var lucky = 7
var unlucky = 13

func swapTwoVariables<T>(inout first: T, inout second: T) {
    let temp = first
    first = second
    second = temp
}

swapTwoVariables(&lucky, &unlucky)

println("lucky: \(lucky)   unlucky: \(unlucky)")
// "lucky: 13   unlucky: 7"
{% endhighlight %}
<!-- /Code ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^--> 
