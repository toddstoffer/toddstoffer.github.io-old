---
title: Adding Reveal.js to Jekyll Academic
date: 2016-05-25 00:00:00 Z
categories:
- blog
tags:
- jekyll
- tutorial
- blog
layout: post
excerpt: Adding reveal.js to Jekyll Academic allows you to host your own dynamic slide
  show right from your GitHub Pages website.
modified: 2016-05-25 12:46:33 Z
comments: false
---

# Adding reveal.js to Jekyll Academic to Create, Host and Present Slide Decks

The addition of reveal.js to your [Jekyll Academic](https://github.com/NCSU-Libraries/jekyll-academic) website allows you to create dynamic slideshows quickly and easily. They are hosted on your GitHub Pages website and play in a browser, so you don't need to worry about software compatibility. The initial setup is somewhat complex, but once that is complete you will be able to simply copy an existing blog post that is formatted for reveal.js, change the content and push to GitHub.

### Step 1 - Add the reveal.js code to your repository
- Download and unzip the reveal.js zip file from [https://github.com/hakimel/reveal.js](https://github.com/hakimel/reveal.js)
- Move the unzipped reveal.js directory into the root directory of your website. This shoudl be in the same directory that contains \_Posts and \_config.yml

### Step 2 - Create a new blog post layout for slide decks
- Copy the content from the slide.htm that can be found [here](https://github.com/toddstoffer/toddstoffer.github.io/blob/master/_layouts/slide.html) into a blank text file.
- Save that file as slide.html into your \_layouts folder.

### Step 3 - Create a test slide deck

Create a new blog post file and paste the following code into that file:

    ---
    layout: slide
    title: test
    excerpt: "test"
    theme: blood
    transition: convex
    tags: [presentation]
    category: presentation
    ---
    <section data-markdown>

    ### Slide 1
    Slide 1 text.

    </section>

    <section data-markdown>

    ### Slide 2

    Slide 2 text.

    </section>

### Step 4 - Sync everything to Github
- Commit changes to GitHub
- Sync changes to GitHub
- Visit your blog post to see your new reveal.js slide Decks

### Step 5 - Editing Your slideshows

#### Overview
As you noticed there should be two slides in your new slide deck. The content for both slides is contained in the one Markdown file. Each slide starts with a `<section data-markdown>` tag and ends with a `</section>` tag. You can add as many slides as you want to a presentation by simply adding new sections to the same Markdown file that you have been editing.

#### Themes
There are a variety of themes to choose from. [This](https://lab.hakim.se/reveal-js/#/themes) page shows you what the different themes look like. In order to update the theme simply change the theme name you are using in your Markdown file. For example change `Theme: blood` to `Theme: sky`.

#### Transitions
Similarly to updating the theme of your slideshow, you are also able to update the transitions used when switching between slides. An example of transitions can be found [here](https://lab.hakim.se/reveal-js/#/transitions). In order to update transitions simply replace the current trasition name with the one you wish to use instead.
