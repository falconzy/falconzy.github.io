---
layout: post
title: "Hello Octopress"
date: 2013-12-26 20:42:38 +0800
comments: true
categories: 
---
**How to setup a Octopress website**

##Octopress Setup (http://octopress.org/docs/setup/)

##Before You Begin

 - Install Git.
 - Install Ruby.

##Setup Octopress

git clone git://github.com/imathis/octopress.git octopress
cd octopress

##install dependencies

gem install bundler
bundle install

Install the default Octopress theme.

rake install

Configuring Octopress(http://octopress.org/docs/configuring/)

##Blog Configuration
In the _config.yml there are three sections for configuring your Octopress Blog. Spoiler: You must change url, and you'll probably change title, subtitle and author and enable some 3rd party services.
- Main Configs
- Jekyll & Plugins
- 3rd Party Settings

##Blog Posts(http://octopress.org/docs/blogging/)

Syntax
New Post

rake new_post["title"]

New Pages

rake new_page[super-awesome]
# creates /source/super-awesome/index.markdown
 
rake new_page[super-awesome/page.html]
# creates /source/super-awesome/page.html



##Generate & Preview

rake generate   # Generates posts and pages into the public directory
rake watch      # Watches source/ and sass/ for changes and regenerates
rake preview    # Watches, and mounts a webserver at http://localhost:4000

##Deploying to Github Pages
Create a new Github repository and name the repository with the format username.github.io, where username is your GitHub user name or organization name. (DO NOT ADD any file inside)

rake setup_github_pages


rake generate
rake deploy

##commit the source for your blog.
git add .
git commit -m 'your message'
git push origin source
