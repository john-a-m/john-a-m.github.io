---
layout: post
title:  "How this blog was built"
date:   2015-11-28 11:35:07
categories: meta
---

[Here is githubs info on this process][5]

##Accounts

get account at pawnmail (they're no longer accepting registrations at this time), or a similar service

have a github account

##Configure your environment

###DNS

	@ 		MX 	mx.pawnmail.com.
	@ 		A 	23.235.39.133
	mail.eden.ai 	A 	107.191.103.103

23.235.39.133 is github's nameserver

107.191.103.103 is pawnmail's mx server [more here][1]

more info here

###Ruby

Get both ruby and the development-kit from [rubyinstaller][2].

Download both the installer and the development-kit

extract the development kit to `C:\ruby-dev-kit` cd into that directory and run 

	ruby dk.rb
	ruby dk.rb install

[Source][3]
	
###Python

Install python from python.org and make sure python.exe is in your PATH.
	
##Set up jekyll

[General Info on this process][4]

create a directory githubusername.github.com, cd into it and run `git init`

add a file `CNAME` put a single line in it `yourhostname.tld`



	gem install bundler

add a `Gemfile` 

	source 'https://rubygems.org'
	gem 'RedCloth', :platforms => :mswin
	gem 'github-pages'

run bunlder
	
	bundle install
	
{% highlight powershell %}

jekyll build
jekyll serve --watch

{% endhighlight %}

now you can make changes to the _config.yaml, add new posts, etc. 

when you're ready to send it out to the world run `git push`

[1]: http://imakewebthings.com/blog/github-pages-email/
[2]: http://rubyinstaller.org/
[3]: https://github.com/oneclick/rubyinstaller/wiki/Development-Kit
[4]: https://help.github.com/articles/using-jekyll-with-pages/
[5]: https://help.github.com/categories/github-pages-basics/