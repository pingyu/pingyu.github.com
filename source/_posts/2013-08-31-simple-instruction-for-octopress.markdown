---
layout: post
title: "Simple Instruction for Octopress"
date: 2013-08-31 23:41
comments: true
categories: [Octopress]
---
referenced from official docs of octopress <http://octopress.org/docs/blogging/>

### New Post ###

	cd /path/to/octopress
	rake new_post['title']
	<edit /path/to/octopress/source/_post/YYYY-mm-dd-title.markdown>
	rake generate
	(if want to preview:
		rake watch
		rake preview (or use [pow](http://pow.cx/))
	)
	rake deploy

ps. Recommend [Mou](http://mouapp.com/) as markdown editor for OSX

### Modify Anything Else ###
e.g. _config.yaml modified

	rake generate
	rake deploy

### Git Push ###
git commit add …

git commit -m'…'

git push origin source
