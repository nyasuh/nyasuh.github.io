---
layout: post
title: "Hyperlinked & Including Images on Jekyll Post "
date: 2015-11-9 03:21:35
description: ''
tags:
- jekyll
categories: 
- jekyll
---

## Including images, pdf & hyperlinked images 

Chances are, at some point, you’ll want to include images, downloads, or other digital assets along with your text content. While the syntax for linking to these resources differs between Markdown and Textile, the problem of working out where to store these files in your site is something everyone will face.

Because of Jekyll’s flexibility, there are many solutions to how to do this. One common solution is to create a folder in the root of the project directory called something like **`assets`** or **`bla bla..`**, into which any images, downloads or other resources are placed. Then, from within any post, they can be linked to using the site’s root as the path for the asset to include. Again, this will depend on the way your site’s (sub)domain and path are configured, but here some examples (in Markdown).   

>>**Including an image in a post :**  
{% highlight bash %}
![anu]({{ site.url }}/assets/img/jekyll.jpg)
{% endhighlight %}

**Will be Show :**
![anu] ({{ site.url }}/assets/img/jekyll.png)  
  
>>**Linking to a PDF for readers to download :** 
{% highlight bash %}
You can [Get the PDF]({{ site.url }}/assets/pdf/rootmagz-042015.pdf) directly.
{% endhighlight %}

**Will be Show :**  
You can [Get the PDF]({{ site.url }}/assets/pdf/rootmagz-042015.pdf) directly.

>> **Hyperlinked Images :**
{% highlight bash %}
[![info] ({{ site.url }}/assets/img/jekyll.png)][jekyll]
[jekyll]: http://jekyllrb.com/docs/posts/#including-images-and-resources/ "Click to visit"
{% endhighlight %}  

**Will be Show :** 
[![info] ({{ site.url }}/assets/img/jekyll.png)][jekyll]
[jekyll]: http://jekyllrb.com/docs/posts/#including-images-and-resources/ "Click to visit"
