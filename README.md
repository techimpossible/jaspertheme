# Jasper

This is a fork of [Casper](caspertheme) for [Ghost](tryghost) for [Jekyll](jekyllrb) instead. Huge thanks to the Ghost team for the theme, it's simply gorgeous.

## Differences
There aren't many differences, the sites should be more or less identical when viewed side-by-side. Pretty much the only difference is the URL for the author page, in Casper it's ````/author/author-name/``` while in Jasper it's just ```/author/```. Other than that it should be a 1:1 fork.

## Getting started
### Installation
Simply clone this repository, go into it and run ````jekyll serve --watch``` and you are good to go!

### Configuration
There aren't too many things to change for this to work, everything you need to change is in the ````_config.yml``` file:

````# Site settings
title: Your awesome title # Title of your site
description: > # this means to ignore newlines until "baseurl:"
  Write an awesome description for your new site here. You can edit this
  line in _config.yml. It will appear in your document head meta (for
  Google search results) and in your feed.xml site description.
baseurl: "" # the subpath of your site, e.g. /blog/
permalink: /:title # Permalink structure
url: "localhost:4000" # the base hostname & protocol for your site
paginate: 5 # Number of posts per page
paginate_path: page/:num #Permalink structure for pagination

author: # You can invoke these via {{ site.author.NAME }} 
    name: Your Name # Change to your name
    bio: >
        Hello world! This is a short bio of who I am, what I'm doing and how awesome I am. # Short and sweet about you
    location: Mars # Where you live (accuracy not guaranteed)
    home: http://example.com # Your website, must include http:// otherwise Jekyll thinks it's an internal link
````

These are all the settings, you can probably already tell what should be changed. Change the URL of your site, your name, bio, location and such and the site is ready to go.

### Publishing your site
#### Github Pages
If you want to publish this to your own Github profile (````username.github.io```) you do not need to do anything, just change the settings, push and you are ready.

#### Project pages
If you however want to host your site in a project page you'll have to do a bit of manual labour. First you need to change the ````baseurl:``` to the name of the repository: ```baseurl: repository-name```, then you'll have to add ```{{ site.baseurl }}``` to all the includes and most of the layouts as it isn't there. This is something that I should probably fix but I couldn't find an elegant way to do it, sadly. You will also have to run the site via ```jekyll serve --watch --baseurl=''```.

# Thanks to
The people beind [Casper](caspertheme), they made a great theme that I really love. Thanks guys!

[caspertheme]: https://github.com/TryGhost/Casper
[tryghost]: https://github.com/TryGhost/Ghost
[jekyll]: http://jekyllrb.com/
