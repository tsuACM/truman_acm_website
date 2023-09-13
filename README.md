# How to Edit the TSU ACM Website

This guide is intended for new Webmasters for the ACM chapter of Truman State University. Please read the following instructions carefully. 

# Requirements
- Understanding of git and Github

# 1. Install jekyll windows
- Install ruby-dev from [this](https://rubyinstaller.org/downloads/) website. Make sure to install version **2.7.8**. 
- Pull the website code to your computer.
- Open a command line in the website directory.
- Type: 

``` 
gem install bundler
```

- While cmd prompt is in the acm directory type: 

```
bundle update
```

- Then you can run: 

```
jekyll build
```

to build the website. 

- If you get this error "You have already activated X, but your Gemfile requires Y" then you can do two things
```
gem uninstall x
```

with x being the version thats newer, or 

``` 
bundle exec jekyll build
```

which will force the use of the version you needed. This works with all the Jekyll commands. 


# 2. Understanding Jekyll
This website uses Jekyll, which compiles plain-text markdown files into HTML files. I highly recommend reading through this Jekyll tutorial, 
starting [here](https://cloudcannon.com/tutorials/jekyll-tutorial/getting-started/). You can also look at the [documentation](https://jekyllrb.com/docs/)
if you have more questions. 

When you pulled the website code, you probably noticed that it has a lot of folders with odd names. 
Jekyll lays out a website's folder structure in a specific way. 

_includes - This folder stores the site's HTML header, footer, and navigation. The header and footer do not need to be edited, but you can
edit navigation.html to change the nav bar at the top of each page. 

All of the main pages are in _pages, except the front page which is just index.markdown in the root directory. They are markdown files that you edit so a minimal amount of html and css knowledge is necessary. 

The meeting minutes are saved in _posts. There is a template for those. just make sure to save it and rename it before you start editing it. 


# Meeting Minutes notes
ACM does not keep minutes for general meetings at this time. However, there still exists an unused page to display minutes on the site. 
Should ACM ever start keeping minutes again, follow these steps to add new minutes: 

- file name should be in the format yyyy-mm-dd-string.md
- title tag will be what is actually displayed on the webpage, so it should be meaningful 
- place files in _posts folder


# material-jekyll-theme
[Demo](http://alexcarpenter.github.io/material-jekyll-theme)

![Material Jekyll Theme](https://d13yacurqjgara.cloudfront.net/users/37718/screenshots/2430279/slice_1.jpg)

## Getting started
1. `git clone https://github.com/alexcarpenter/material-jekyll-theme.git`
2. `cd material-jekyll-theme`
3. Configure the `_config.yml` file as needed
4. `jekyll serve`

## Options
Customize your options within the `_config.yml` file.

+ Theme
  - Green
  - Blue
  - Orange
  - Purple
  - Grey
+ Fixed Navigation
  - True
  - False
