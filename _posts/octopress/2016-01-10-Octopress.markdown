---
layout: post
title:  "Octopress"
date:   2016-01-10 00:49:37
description: ''
tags:
- octopress
categories: 
- octopress
---


### What is Octopress ?
Octopress is a framework designed for Jekyll, the static blogging engine powering Github Pages. Have a look through the documentation and if you have trouble, [I'll be happy to help][help]. If you find errors in the [documentation post an issue](issue) or fork and send a pull request to the [master branch][doc]

### Octopress Setup
1.  ``` install git ```
2. ```install ruby ```  
3. ``` git clone git://github.com/imathis/octopress.git octopress ```
4.  ```cd octopress ```

### install dependecies
1. ```gem install bundler```
2. ```bundle install```

### Install the default Octopress theme.
1. ```rake install ```

### Deploying to Github Pages
Use this if you want to host a blog from `http://username.github.io` (though you can also use custom domains ). In the past, Github has used `http://username.github.com` for these domains, but is shifting to the 'io' extension instead for Pages.  

Create a [new Github repository][git] and name the repository with the format `username.github.io`, where `username` is your GitHub user name or organization name.

Github Pages for users and organizations uses the master branch like the public directory on a web server, serving up the files at your Pages url `http://username.github.io` As a result, you'll want to work on the source for your blog in the source branch and commit the generated content to the master branch. Octopress has a configuration task that helps you set all this up.  
####then :  
1. `rake setup_github_pages`

The rake task will ask you for a URL of the Github repo. Copy the SSH or HTTPS URL from your newly created repository (e.g. `git@github.com:username/username.github.io.git` OR `https://github.com/username/username.github.io`) and paste it.  

#### Next run:
1. `rake generate`
2. `rake deploy`

This will generate your blog, copy the generated files into `_deploy/` add them to git, commit and push them up to the master branch.

Then commit the source for your blog.  
1. `git add . `  
2. `git commit -m 'fush' `  
3. `git push origin source `  

### Custom Domains  
First you'll need to create a file named CNAME in your blog's source:  
{% highlight ruby %}
echo 'your-domain.com' >> source/CNAME
# OR
echo 'www.your-domain.com' >> source/CNAME
{% endhighlight %}

### Note 
>> Do not use a CNAME record with a top-level domain! It can have adverse side effects on other services like email. Many DNS services will let you set a CNAME on a TLD, even though you shouldn’t. Remember that it may take up to a full day for DNS changes to propagate, so be patient.

##### Source : [Github pages guide][github]
[github]: https://help.github.com/categories/github-pages-basics
[git]: https://github.com/new
[help]:  http://octopress.org/help  
[issue]:  https://github.com/octopress/docs/issues  
[doc]:  https://github.com/octopress/docs/tree/master  