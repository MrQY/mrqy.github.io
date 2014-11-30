---
layout: post
title: "jekyll快速开始"
description: "jekyll快速开始"
category: lessons
tags: [jekyll]
---
{% include JB/setup %}
#1.Create a Post
Create posts easily via rake task:
	
	$ rake page name="about.md"
Create a nested page:
	
	$ rake page name="pages/about.md"
Create a page with a "pretty" path:
	
	$ rake page name="pages/about"
	# this will create the file: ./pages/about/index.html
The rake task automatically creates a page file with properly formatted filename and YAML Front Matter as well as includes the Jekyll Bootstrap "setup" file.

----------
#2.Publish
After you've added posts or made changes to your theme or other files, simply commit them to your git repo and push the commits up to GitHub.
	
	$ git add .
	$ git commit -m "Add new content"
	$ git push origin master

----------
#3.Install Themes
Install a theme by using the rake task and passing in the theme's git url.
	
	$ rake theme:install git="https://github.com/jekyllbootstrap/theme-the-program.git"
The installer uses git to download the Theme Package and then installs it. If you have obtained a Theme Package in another way, such as zip download, you can manually place it into your ./_theme_packages folder and then run the installer with the name of the theme.
	
	$ rake theme:install name="THEME-NAME"
As a convenience, after the install is successful, the task will ask you if you'd like to switch to the newly installed theme. Type 'y' and enter to switch!

----------
#4.Switch Themes
Once your themes are installed you can switch between them via rake task:
	
	$ rake theme:switch name="the-program"
	# for 0.1.0 users `rake switch_theme` still works.