---
layout: post
title: Creating portfolio-blog site using the coda-jekyll-theme-starter
tags: blogs jekyll portfolio
category: jekyll
featured: true
date: '2020-01-01'
image: https://sonumeewa.github.io/assets/img/blogs/1.png
---

Hello developers, I am here to help you use the coda-jekyll-theme to build jekyll portfolio-blog websites. coda-jekyll-theme is not a full fledged theme, but only a boilerplate to build a personal portfolio-blog like [this](https://sonumeewa.github.io)

## Prerequisite

- jekyll and bundler to be installed in your system
- Github Account (required to host your site on github pages)
- coda-jekyll-theme-starter code, you can download it [here](https://github.com/sonumeewa/coda-jekyll-theme-starter)

## Installation and usage

- Fork and clone the above mentioned starter code.
- Change the variables in the **config.yml** file according to your site. ( base_url, github username etc.). Variables and thier usage is explained in upcoming sections.
- Run command `bundle exec build --trace` to build the project.
- If you get an error regarding the dependencies, you may install them using `sudo bundle install`.
- If you get an error for unmatched version of jekyll for github pages, you can fix that by installing the jekyll version currently being supported by the "github-pages" gem (3.8.5 yet).
- If the build is done without any errors, you can now use `bundle exec serve --watch` command to serve the jekyll site locally on [localhost:4000](http://localhost:4000/)
- The text in the site is fetched from a yaml file named as "default.yml" in the "\_data" folder of the project, go ahead and change the value of the variables to reflect your text in the site.
- finally push all of the contents to your "username.github.io" where username is your github username. It will be live.

## Variables in config.yml

- **title** : The title for your site. This variable is being used in the jekyll-seo-tag plugin to assign the title meta tag for your websites pages (other than post pages).
- **email** : The email adress of the owner of the site.
- **description** : The description for your site. This variable is being used in the jekyll-seo-tag plugin to assign the description meta tag for your websites pages (other than post pages).
- **url** : The url for your site. This variable is being used in the jekyll-sitemap plugin to build the sitemap of your website
- **discus.shortname ( optional )** : The discuss shortname for your site. This variable is being used in the theme to enable comments on the posts. You can sign up on discuss and get your shortname [here](https://disqus.com/) . You can leave it blank if you don't want the comments to be enabled on your posts. You can disable post on individual posts by having `comments: false` in the front matter for your post.
- **google_analytics ( optional )** : The Google analytics ID for your site. This variable is being used in the theme tomonitor traffic on yout site. You can leave it blank if you don't want to monitor traffic.
- **paginate**: The number of posts to show in the paginated list on the blog listing page.
- Here is my config.yml

## Adding posts

- You can add posts in the \_posts folder and assign it variables for the post details like title, description, image etc.
- You'll have to name your posts markdown file in the format YEAR-MONTH-DATE-TITLE.md where year, month and date belongs to the date of writing the post and title is title of the post.
- The layout in the frontmatter of the post should be "post"
- The tags and categories are used to create section in the post list page, you can add tags and categories in the frontmatter. The only thing to take care of is you should have a .html file doe each of the tag and category in the "/blog/tags/" and "blog/categories/' folders respectively. These .html files are used to list all the blogs of that tag or category.
- You don't need to any content on those .html pages, just add `layout: tagpage`or `layout: catpage` and after it add `tag: "your tag name"` or `category: "your category name"` .
- Your tags and categories will automatically be listed in the tags and categories list in the sidebar of blog page. They will link to the pages listing all the blogs of that tag or category automatically.
- Here is a sample blog post screenshot

## Follow up

If you get error in installation or running the theme, feel free to use the comments section.
