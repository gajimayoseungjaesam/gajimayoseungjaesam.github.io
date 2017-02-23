# Jekyll Tutorials Template

This is a blog/tutorial website template using Jekyll. 

## Live Demo
https://jarellano01.github.io/template_jekyll-tutorials/

## Features
- Bootstrap template
- Modularized layouts and partials
- Deployable to github pages
- 3 ways to add webpages to your site
    + _posts is meant for blog type articles
    + _pages are navigation pages that do not change constantly, such as home, All Tutorials, or All Posts. Meant for display purpose only
    + _tutorials is meant for structured tutorials that are meant to be organized in a specific fashion. See examples based on Bluebeam Revu. 

## Adding Custom Bootstrap
This template has already been set up with a simple bootstrap design and custom css. Feel free to add your own design. Here are a few guidelines for ensuring that the original functionality still works. 

### _layouts
The layouts folder contains 3 files: default.html, post.html, and tutorial.html. 

#### default.html
- Add boilerplate html
- Add css and js dependencies 
- Navbar code can be placed inside of _includes/navbar.html
- Be sure to always have `{{ content }}` somewhere in your body. All pages and templates using default.html as the base template will be rendered into this section. 

#### post.html and tutorial.html
- Be sure to always include the jekyll front matter including the three `-` above and below. This will specify that this page should be rendered inside of the default.html in the `{{ content }}` area which I mentioned before.
```
---
layout: default
---
```
- These templates will add next and previous buttons at the bottom of each post or tutorial. This feature may be removed if not desired by deleting the following lines of html: 
```
<div class="row">
    <div class="col-xs-12 text-center">
        {% if page.previous.url %}<a class="btn btn-default" href="{{page.previous.url | prepend:site.baseurl }}">Previous</a>{%
        endif %}
        <a class="btn btn-default" href="{{site.baseurl}}/tutorials">Back to Main</a>
        {% if page.next.url %}<a class="btn btn-default" href="{{page.next.url | prepend:site.baseurl }}">Next</a>{%
        endif %}
    </div>
</div>
```

## Adding New Posts
- Create a new markdown file inside of `_posts` and name it in the following format: 
`yyyy-mm-dd-name-of-post`
- Inside this file add the following basic template: 
```
---
layout: post
title:  "Name of Post"
date:   2016-12-12 11:18:08 -0800
categories: intro welcome
---
{:.post-intro}
**First line will be used as the intro when displayed in the Tutorials and Posts pages. Be sure to add a good intro line.**

Anything after the first line will be the rest of your tutorial/post. Use regular markdown language to format your page. 
```

## Adding New Tutorials
- Create a new markdown file inside of `_posts`.
- Naming matters as it will be sorted alpha-numerically
    + See `_tutorials/bluebeam` for an example on how to organize your tutorials
- Inside this file add the following basic template: 
```
---
categories: intro welcome
---
{:.post-intro}
**First line will be used as the intro when displayed in the Tutorials and Posts pages. Be sure to add a good intro line.**
 
Anything after the first line will be the rest of your tutorial/post. Use regular markdown language to format your page. 
```
- Tutorials will automatically use tutorial.html as their layout. 


