---
layout: post
title: "Setup Octopress on my MacOS"
date: 2013-09-05 21:41
comments: true
categories: [Octopress]
---
To describe the setup process on my Mac OS 10.8.

Referenced from <http://octopress.org/docs/setup/>

1. Download Octopress
> git clone git://github.com/imathis/octopress.git octopress

1. Install ruby 1.9.3. (Note that only ruby 1.9.3, NOT 1.9.3 or above)
> brew install rbenv
> 
> brew install ruby-build
> 
> rbenv install 1.9.3-p0
> 
> rbenv rehash
>

1. Modify content of .ruby-version file in octopress to "1.9.3-p0". Run "ruby --version" should report "Ruby 1.9.3-p0"

1. Final setup commands
> gem install bundler
> 
> rbenv rehash
> 
> bundle install
> 
> rake install

