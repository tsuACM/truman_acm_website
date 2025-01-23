# _includes
This folder stores the site's HTML header, footer, and navigation. 


### Footer
The footer lists our social medias. You might notice that each social media link in this file follows a formatting like 
```
{% if site.username %}<a href="https://socialmedia.com/{{ site.username }}">Social Media</a>{% endif %}
``` 
The variable `site.username` is a variable found in `_config.yml` in the main acm folder. That variable is our handle for that social media. 
For example, the variable for Github in `_config.yml` is "tsuACM", so in the HTML line 
```
{% if site.githubUsername %}<a href="https://github.com/{{ site.githubUsername }}">Github</a>{% endif %}
```
the variable `{{ site.githubUsername }}` would be replaced with tsuACM, resulting in [this link](https://github.com/tsuACM). 

If you need to edit our social media handles, you *only* need to edit `_config.yml`. If the social medias we use change, make sure to add or remove the appropriate lines in `footer.html`. 


### Navigation
You can edit `navigation.html` to change the nav bar at the top of each page. Each link in the bar is formatted like
```
<a class="c-navigation__item {% if page.url == 'events/' %}is-active{% endif %}" href="{{ "/events/" | prepend: site.baseurl }}">Events</a>
```

You might notice that some of these pages have markers around them: `<!-- -->`. These mark the lines as comments, and these links will not appear on the website. We have preexisting pages for our yearly Codeathons and Game Jams, as well as a page for T-shirt sales. To activate these pages, remove those comment markers and rebuild the site. To deactivate the pages, simply add the comment markers back and rebuild. 


### Other Files

`button.html` - Creates a button with the text "ORDER HERE". This is used on the T-shirt order page. 

`discord.html` - Creates a widget that displays information about our Discord server. This is used on the About page. 

`head.html` - This just adds important metadata to each page. Avoid editing this file.