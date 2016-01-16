---
layout: post
title:  "Jekyll"
date:   2015-11-08 00:49:37
description: ''
tags:
- jekyll
categories: 
- jekyll
---

### What is jekyll ?
Jekyll is a simple, blog-aware, static site generator perfect for personal, project, or organization sites. Think of it like a file-based CMS, without all the complexity. Jekyll takes your content, renders Markdown and Liquid templates, and spits out a complete, static website ready to be served by Apache, Nginx or another web server. Jekyll is the engine behind [GitHub Pages] [github] which you can use to host sites right from your GitHub repositories.  

### Quick start 
{% highlight ruby %}
$ gem install jekyll
$ jekyll new my-awesome-site
$ cd my-awesome-site
$ jekyll serve
# => Now browse to http://localhost:4000 
{% endhighlight %}

### Deploy to Github pages
1. Create a repository and name repository with format ` username.github.io  `
2. Clone the repository {% highlight ruby %}$ git clone https://github.com/username/username.github.io {% endhighlight %}
3. Create site {% highlight ruby %}$ jekyll new site{% endhighlight %}
4. Move all in site {% highlight ruby %}$ mv site/* username.github.io {% endhighlight %}
5. Enter the project folder {% highlight ruby %}$ cd username.github.io{% endhighlight %}
6. Push it : {% highlight ruby %}
$ git add --all
$ git commit -m "fush"
$ git push -u origin master{% endhighlight %}
7. You're done, go to `http://username.github.io`

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[github]: https://pages.github.com
[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
