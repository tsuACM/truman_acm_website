# _includes
This folder stores the site's HTML header, footer, and navigation. The header contains basic HTML info that doesn't need to be edited. 
You can edit `navigation.html` to change the nav bar at the top of each page should a new page be necessary. 

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

If you need to edit our social media handles, you *only* need to edit `_config.yml`. If the social medias we use change, make sure
to add or remove the appropriate lines in `footer.html`. 

