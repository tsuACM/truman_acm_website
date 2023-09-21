# How to Edit the TSU ACM Website

This guide is intended for new Webmasters for the ACM chapter of Truman State University. Please read the following guide carefully to understand the website. 

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

### Folders

When you pulled the website code, you probably noticed that it has a lot of folders with odd names. 
Jekyll lays out a website's folder structure in a specific way. 

`_includes` - This folder stores the site's HTML header, footer, and navigation.

`_layouts` - These HTML documents describe how different types of pages should be put together. They generally do not need to be edited. 

`_pages` - This folder contains the actual content for the website's pages. These files will be edited most frequently. 

`_posts` - These contain old meeting minutes. Minutes are no longer recorded or displayed on the site, so this folder goes unused. 

`_sass` - This folder stores all of the site's CSS themes and do not need to be edited. 

`_site` - When you build the site, the compiled HTML and CSS are stored in this folder. **Do not edit the contents of this folder**, as any
changes made in here will be overwritten when you build the site. 

`assets` - Contains files that appear on the website such as images and code. 

`css` - Contains main.scss, which tells jekyll how to pull the CSS files in `_sass` into a complete CSS style sheet. Does not need to be edited. 

Each folder has its own README.md that contains a little more information on that folder. 

### Files
There are a few important files in the main acm folder that you need to know about. 

`index.markdown` - This is the home page for the website. To edit the home page, just edit this file and build the site. 

`_config.yml` - This file stores all of the website's variables, from the title to our social media handles. Read all of the information at the top of the 
file. Feel free to edit items under the "Social" heading, but leave everything under "Build settings" alone unless you are confident in what you're doing. 


# 3. Changing the Website
After making edits to the site, make sure to use 
```
jekyll build
```
to compile the changes into `_site`. Keep in mind that the links used in the HTML depend on the base URL of the website defined in `_config.yml`, 
so many features such as styling and images will not work properly on your local machine. If you are satisfied with the changes, go ahead and 
push your code. Once your code has been edited and pushed, you need to pull it onto the web server: 

- Log into Truman's Linux server at *sand.truman.edu*.
- Navigate to *var/www/html/acm* and open the console
- Pull your changes
- Open *acm.truman.edu* to ensure your changes went through

Congratulations! That's everything you need to know to edit the website. 




# Other Items

## material-jekyll-theme
This section is a remnant of the original jekyll theme used for the site. 

[Demo](http://alexcarpenter.github.io/material-jekyll-theme)

[Theme Repository](https://github.com/alexcarpenter/material-jekyll-theme)

![Material Jekyll Theme](https://d13yacurqjgara.cloudfront.net/users/37718/screenshots/2430279/slice_1.jpg)

### Getting started
1. `git clone https://github.com/alexcarpenter/material-jekyll-theme.git`
2. `cd material-jekyll-theme`
3. Configure the `_config.yml` file as needed
4. `jekyll serve`

### Options
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
