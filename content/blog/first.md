---
title: "The lazy man's blog"
date: 2017-10-15T13:15:06-04:00
draft: false
---

# A static blog.. The simplest way possible.

I am a big fan of keeping this simple, especially to start. With side projects I've found that I have a tendency
to obsess over finding the exact right solution for the job. This leads me to come up with some sort of 
over engineered mess that will ultimately never see the light of day. Picking a blogging solution
was no exception to this.

Finally, one rainy Sunday afternoon I decided, enouch research or designing, I'm going to use a static site 
generator and hack together any features I realize I need down the road.

This is how I set up my blog.. the simplest way I could find. 


## Picking a static site generator

I googled static site generators. The first link that came up (www.staticgen.com)[www.staticgen.com] gave me a bunch of options.
I sorted by # of stars and fought the urge to research if MIT or APL 2 is a more permissive license. I went with Hugo 
because I am irrationally averse to Ruby and kept on going.

## Getting started

Creating a new project is dead simple. Just run 
``` hugo new site blog```

and a new directory named blog with a hugo project is generated.

The new directory structure looks like this:
```
+ blog 
|
+ --- config.toml
|
+ --- content/
|
+ --- data/
|
+ --- layouts/
|
+ --- static/
|
+ --- themes/
```

## Picking a theme

I took a quick look at (https://themes.gohugo.io)[https://themes.gohugo.io]. Normally I would spend
days hemming and hawing over which theme would be perfect. Today I decided, lets just keep it simple. 
I saw the (Goa)[https://themes.gohugo.io/hugo-goa/] theme with a picture of Erlich Bachman and decided it was a winner.
Installing a new theme with hugo is dead simple. Just cd into the themes directory and clone the themes git repository.
``` bash
git clone https://github.com/shenoybr/hugo-goa 
```

The directory should now look like this:
```
+ blog 
|
+ --- config.toml
|
+ --- content/
|
+ --- data/
|
+ --- layouts/
|
+ --- static/
|
+ --- themes/
	|
	+ hugo-goa
		|
		+ archetypes
			|
			+ default.md
		+ exampleSite <- excluded example site files for brevity
		|
		+ images 
			|
			+ screenshot.png
			|
			+ tn.png
		+ layouts
			|
			+ _default
				|
				+ list.html
				|
				+ single.html	
			+ partials
				|
				+ avatar.html
				|
				+ content.html
				|
				+ error.html
				|
				+ footer.html
				|
				+ header.html
				|
				+ info.html
				|
				+ li.html
				|
				+ main_menu.html
				|
				+ menu.html
				|
				+ social.html
				|
				+ sub_footer.html
			+ 404.html
			+ index.html
		+ static <-- excluded listing static assets for brevity

```

## Futz with the configuration

Hugo is using the config.toml file to configure the application. I copied the configuration supplied in the theme's example site and then changed the values until all of the Erlich refrences were gone.
