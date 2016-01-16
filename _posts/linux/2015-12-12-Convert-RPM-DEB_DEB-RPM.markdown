---
layout: post
title:  "Convert DEB to RPM (RPM to DEB)"
date:   2015-12-12 00:49:37
description: ''
tags:
- linux
categories: 
- linux
---

### Install alien command on Debian / Ubuntu
{% highlight ruby %}
$ sudo apt install alien
{% endhighlight %}  

### Convert rpm to deb file ###
{% highlight ruby %}
$ sudo alien light_43.0-2.20160113145239_amd64.rpm   
light_43.0-2.20160113145239_amd64.deb generated
{% endhighlight %} 

### Convert deb to rpm file ###
{% highlight ruby %}
$ sudo alien light_43.0-2.20160113145239_amd64.deb   
light_43.0-2.20160113145239_amd64.rpm generated
{% endhighlight %} 

### Convert to SLP, LSB, Slackware TGZ packages
#### You can also use alien command to convert files to Stampede slp package, LSB package, and Slackware tgz package. Do `alien -h` to see available options.
![anu] (/assets/img/alien.png)