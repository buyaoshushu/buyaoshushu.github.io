---
layout: post
title: javascript学习笔记
date: 2015-08-15
category: 学习笔记
tags: [javascript]
---

##取最小值
{% highlight javascript %}
Math.min.apply(Math, arr)
{% endhighlight %}
##数组排序
{% highlight javascript %}
var arr=[1,0,2];
arr.sort();
{% endhighlight %}
##字符串转数字数组
{% highlight javascript %}
var good="1 2 3 4 5";
var g = good.split(" ").map(function(x){return parseInt(x)});
{% endhighlight %}
