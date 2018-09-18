---
layout: slide
title: Going off the Rails on a Jekyll Train
excerpt: "You want to build a blazingly fast, secure and feature-rich website. Perhaps it needs to include dynamic features like search, responsive design and easy editing options for content creators. A static website might not be the first tool that comes to mind to accomplish this task, but it might actually be exactly what you are looking for."
theme: simple
transition: slide
tags: [presentation]
category: presentation
---

<section data-markdown>

# Going off the Rails on a Jekyll Train
March 8, 2017 | Code4Lib | Los Angeles, CA


</section>

<section data-markdown>

# Red, White and Black at NC State
[https://go.ncsu.edu/c4lib17](https://go.ncsu.edu/c4lib17)
</section>

<section data-markdown>

## Mobile Apps Were Trendy
</section>

<section data-markdown>

## So We Built One
![Old Red, White Black](/images/c4l17/old-iphone.png)
</section>

<section>

<h4>People Liked It</h4>
<img src="/images/c4l17/libraries-trend.png">
<p><span style="font-size: 10pt;">Source: American Libraries Magazine (https://americanlibrariesmagazine.org/2013/01/21/universitys-app-provides-tour-of-black-history/)</span></p>
</section>

<section data-markdown>

# but...
</section>

<section data-markdown>

# New Apps Get Old

</section>


<section data-markdown>

# Old Apps Get Expensive

</section>

<section data-markdown>

# What Should We Do?

</section>

<section data-markdown>

### What if we can remove the vast majority of the technical overhead while keeping all of the functionality?

</section>
<section data-markdown>

# We Can
### ...and we did!

</section>

<section data-markdown>

# Our Solution
  - Jekyll
  - Google Spreadsheets
  - lunr.js

</section>

<section data-markdown>

# Jekyll

</section>

<section data-markdown>
### Jekyll Structure

```
├── Gemfile
├── Gemfile.lock
├── LICENSE
├── README.md
├── _config-production.yml
├── _config-staging.yml
├── _data
│   ├── cluster
│   │   └── locations.yaml
│   └── events.csv
├── _events
│   ├── 1889-former-slave-begins-50-year-career-at-university.md
│   ├── 1953-dairy-farm-conference-segregated-dining.md
│   ├── 1953-first-african-american-graduate-students-admitted.md
│   ..........
├── _includes
│   ├── events.html
│   ├── footer.html
│   ├── head.html
│   ├── header.html
│   └── places.html
├── _layouts
│   ├── default.html
│   └── search.html
├── _pages
│   ├── about.html
│   ├── events.md
│   ├── index.md
│   └── places
│       ├── carter-finley-stadium.md
│       ├── chancellors-residence.md
│       ├── dh-hill-library.md
│       ├── free-expression-tunnel.md
│       ├── gardner-hall.md
│   ...........
├── build_scripts
│   ├── event-page-generation.py
│   ├── location-yaml-generation.py
│   ├── places-page-generation.py
│   ├── production-build.sh
│   └── staging-build.sh
├── css
│   ├── bundle.css
│   ├── custom.css
│   ├── fonts
│   └── original\ css
├── favicon.ico
├── images
│   ├── bio-photo.jpg
│   ├── ncsu-library-logo-white.png
│   └── rwb.png
├── js
│   ├── app.js
│   ├── lunr.min.js
│   ├── search.js
│   ├── vendor
│   │   ├── foundation.js
│   │   ├── jquery.js
│   │   └── what-input.js
│   └── vendor.min.js
└── search.html
```
</section>

<section data-markdown>

### Jekyll Page
![Event Page](/images/c4l17/eventpage.png)

</section>


<section data-markdown>

# Google Spreadsheets as a CMS

</section>

<section data-markdown>

### This
![Old-RWB-Admin](/images/c4l17/old-admin.png)

</section>

<section data-markdown>

### Becomes..
![Old-RWB-Admin](/images/c4l17/new-admin.png)

</section>

<section data-markdown>

# lunr.js
Like a client-side Solr

</section>

<section data-markdown>

### lunr.js
![Old-RWB-Admin](/images/c4l17/search.png)


</section>


<section data-markdown>


![Build Process Diagram](/images/c4l17/build.png)

</section>

<section data-markdown>

# Results

</section>

<section data-markdown>

#### Original Desktop
![Build Process Diagram](/images/c4l17/desktop-old.png)
</section>

<section data-markdown>

#### New Desktop
![Build Process Diagram](/images/c4l17/new-desktop.png)
</section>

<section data-markdown>

#### Mobile Before and After
![Build Process Diagram](/images/c4l17/mobile.png)
</section>


<section data-markdown>

#Next Steps
- IIIF Integration
- Content Updates

</section>
<section data-markdown>

# Questions?
[Todd Stoffer | NCSU Libraries | tdstoffe@ncsu.edu](mailto:tdstoffe@ncsu.edu)  [@toddstoffer](www.twitter.com/toddstoffer)

</section>
<section data-markdown>

# Resources
- [Red, White & Black at NCSU](https://go.ncsu.edu/c4lib17)
- [Jekyll](https://jekyllrb.com)
- [lunr.js](https://lunrjs.com)

</section>
