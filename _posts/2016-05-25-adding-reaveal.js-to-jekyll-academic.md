---
layout: post
title: Adding Reveal.js to Jekyll Academic
excerpt: "Adding reveal.js to Jekyll Academic allows you to host your own dynamic slide show right from your GitHub Pages website."
modified: 2016-05-25 12:46:33
tags: [jekyll, tutorial, blog]
comments: false
category: blog
---

# Adding reveal.js to Jekyll Academic to Create, Host and Present Slide Decks

The addition of reveal.js to Jekyll Academic allows you to create dynamic slideshows quickly and easily. They are hosted on your GitHub Pages website and play in a browser, so you don't need to worry about software compatibility. The initial setup is somewhat complex, but once that is complete you will be able to simply copy an existing blog post that is formatted for reveal.js, change the content and push to GitHub.

### Step 1
- Download and unzip the reveal.js zip file from [https://github.com/hakimel/reveal.js](https://github.com/hakimel/reveal.js)
- Move the unzipped reveal.js directory into the root directory of your website. This shoudl be in the same directory that contains \_Posts and \_config.yml

### Step 2
- Copy the content from the slide.htm that can be found [here](https://github.com/toddstoffer/toddstoffer.github.io/blob/master/_layouts/slide.html) into a blank text file.
- Save that file as slide.html into your \_layouts folder.

### Step 3

Create a new blog post file and paste the following code into that file:

    ---
    layout: slide
    title: Slide Title
    excerpt: "Slide Excerpt"
    theme: simple
    transition: convex
    tags: [presentation]
    category: presentation
    ---
    <section data-markdown>
      <script type="text/template">
        ## Slide 1 title

        A paragraph with some text and a [link](http://hakim.se).
        </script>
    </section>

    <section data-markdown>
        <script type="text/template">
          ## Slide 1 title

          A paragraph with some text and a [link](http://hakim.se).
          </script>
    </section>

### Step 4
- Commit changes to GitHub
- Sync changes to GitHub
- Visit your blog post to see your new reveal.js slide 
