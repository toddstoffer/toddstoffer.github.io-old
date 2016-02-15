---
layout: post
title: Site Setup and Configuration
excerpt: "What goes where, and how to configure your new site "
modified: 2/12/2016, 8:59:34 AM
tags: [intro, intermediate, jekyll, tutorial]
comments: true
---

# (Almost) Everything You Want to Know About Your New Site


## Getting Started: Step 1
The first step in configuring your new site is to update the two main configuration files for the site. Both of these files are found in the root directory of the site (mysite folder). They are the **_config.yaml** and accent.scss files. The **_config.yaml** contains many of the main configuration settings for your site. It allows you to set a site name, and connect your site to many popular services and platforms such as Github, Twitter and email. The **accents.scss** file allows you to adjust the accent colors of your website (the two lines of color below the navigation). After adjusting these files be sure to safe the files and sync your changes back up to Github.

#### Folder Structure

    mysite/

    Edit these files first:

    |── _config.yaml                 # main site configuration settings, edit this file **first**
    |── accents.scss                 # set site accent colors, edit this file **second**
    ├── about/                       # sample about page, edit this file **third**
    ├── images/                      # images for posts and pages, use this to set bio image and logo
    ├── index.md                     # sample homepage. lists 5 latest posts
    ├── _posts/                      # MarkDown formatted posts
    ├── _data/navigation.yaml        # Add items to site navigation bar

    These files likely do not need editing unless you plan on making major changes to your site:

    ├── _includes/
    |    ├── _author-bio.html        # bio stuff layout. pulls optional owner data from _config.yml
    |    ├── _browser-upgrade.html   # prompt to install a modern browser for < IE9
    |    ├── _disqus_comments.html   # Disqus comments script
    |    ├── _footer.html            # site footer
    |    ├── _head.html              # site head
    |    ├── _navigation.html        # site top navigation
    |    ├── _open-graph.html        # Twitter Cards and Open Graph meta data
    |    └── _scripts.html           # site scripts
    ├── _layouts/
    |    ├── home.html               # homepage layout
    |    ├── page.html               # page layout
    |    ├── post-index.html         # post index layout
    |    └── post.html               # single post layout
    ├── posts/                       # sample post index page. lists all posts in reverse chronology
    ├── _sass/                       # Sass stylesheets
    ├── _templates/                  # used by Octopress to define YAML variables for new posts/pages
    ├── assets/
    |    ├── css/                    # compiled stylesheets
    |    ├── fonts/                  # webfonts
    |    ├── js/
    |    |   ├── _main.js            # main JavaScript file, plugin settings, etc
    |    |   ├── plugins/            # scripts and jQuery plugins to combine with _main.js
    |    |   ├── scripts.min.js      # concatenated and minified _main.js + plugin scripts
    |    |   └── vendor/             # vendor scripts to leave alone and load as is
    |    └── less/
    ├── 404.md                       # 404 page

## Navigation: Step 2
The default site template includes navigation items for your home page (recent posts), About Me, Blog Archive and Resume pages. If you would like to add additional pages to the navigation of your site you can do so by creating a copy of the **about** folder and giving the name of the new page you would like. Once that is done, open _data/navigation.yaml and create a new navigation element that points to the folder you just created.

    Example:
    To create a 'Presentations' page
    1) Copy /about and rename to /presentations
    2) Open /_data/navigation.yaml
    3) Add the following lines:
       - title: Presentations
       url: /presentations/
    4) Save the file, sync changes to Github


### Adding New Pages



## Images
  - default images (logo.png/biopic)

## Includes
What are they, why do they matter


## Posts
What are they, why do they matter
timestamps


## Layouts
what layouts to use and when, how to change a layout, pics of each of the layouts

## License

Figure out the best license for us.
