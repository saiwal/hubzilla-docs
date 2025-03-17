# Customization

## Plugins/Apps

## Themes

### Creating a Derived Theme

A derived theme takes most of the settings from its "parent" theme and lets you change a few things to your liking without creating an entire theme package. 


To create a derived theme, first choose a name. For our example we'll call our theme 'mytheme'. Hopefully you'll be a bit more creative. But throughout this document, wherever you see 'mytheme', replace that with the name you chose.

#### Directory Structure

First you need to create a theme directory structure. We'll keep it simple. We need a php directory and a css directory. Here are the Unix/Linux commands to do this. Assume that 'mywebsite' is your top level $Projectname folder. 


    cd mywebsite
    mkdir view/theme/mytheme
    mkdir view/theme/mytheme/css
    mkdir view/theme/mytheme/php


Great. Now we need a couple of files. The first one is your theme info file, which describes the theme.

It will be called view/theme/mytheme/php/theme.php (clever name huh?)

Inside it, put the following information - edit as needed

    <?php

    /**
     *   * Name: Mytheme
     *   * Description: Sample Derived theme
     *   * Version: 1.0
     *   * Author: Your Name
     *   * Compat: Red [*]
     *
     */

    function mytheme_init(&$a) {

        App::$theme_info['extends'] = 'redbasic';


    }


Remember to rename the mytheme_init function with your theme name. In this case we will be extending the theme 'redbasic'. 


Now create another file. We call this a PCSS file, but it's really a PHP file.

The file is called view/theme/mytheme/php/style.php

In it, put the following:

    <?php

    require_once('view/theme/redbasic/php/style.php');

    echo @file_get_contents('view/theme/mytheme/css/style.css');



That's it. This tells the software to read the PCSS information for the redbasic theme first, and then read our CSS file which will just consist of changes we want to make from our parent theme (redbasic). 

Now create the actual CSS file for your theme.  Put it in view/theme/mytheme/css/style.css (where we just told the software to look for it). For our example, we'll just change the body background color so you can see that it works. You can use any CSS you'd like. 


    body {
        background-color: #DDD;
    }


You've just successfully created a derived theme. This needs to be enabled in the admin "themes" panel, and then anybody on the site can use it by selecting it in Settings->Display Settings as their default theme.  

#### Schemas

If you want to use the redbasic schemas for your derived theme, you have to do a bit more.

Do everything as above, but don't create view/theme/mytheme/php/style.php, but copy instead  view/theme/redbasic/php/style.php to view/theme/mytheme/php/style.php. Modify that file and remove (or comment out) these two lines:

	if(local_channel() && App::$channel && App::$channel['channel_theme'] != 'redbasic')
		set_pconfig(local_channel(), 'redbasic', 'schema', '---');
	
Also add this line at the bottom:

	echo @file_get_contents('view/theme/mytheme/css/style.css');

To show the schema selector you have to copy view/theme/redbasic/tpl/theme_settings.tpl to  view/theme/mytheme/tpl/theme_settings.tpl. Modify that file and replace the lines:

	{{if $theme == redbasic}}
	{{include file="field_select.tpl" field=$schema}}
	{{/if}}

with:

	{{include file="field_select.tpl" field=$schema}}
	
### Theme development - a guide to the schema system


A schema, in a nutshell, is a collection of settings for a bunch of variables to define
certain elements of a theme.  A schema is loaded as though it were part of config.php
and has access to all the same information.  Importantly, this means it is identity aware,
and can be used to do some interesting things.  One could, for example, restrict options
by service class, or present different options to different members.

By default, we filter only by whether or not expert mode is enabled.  If expert mode is
enabled, all options are presented to the member.  If it is not, only scheme, background
image, font face, and iconset are available as choices.

A schema is loaded *after* the member's personal settings.  Therefore, to allow a member
to overwrite a particular aspect of a schema you would use the following syntax:

        if (! $foo)
            $foo = 'bar';

However, there are circumstances - particularly with positional elements - where it
may be desirable (or necessary) to override a member's settings.  In this case, the syntax
is even simpler:

            $foo = 'bar';

Members will not thank you for this, however, so only use it when it is required.

If no personal options are set, and no schema is selected, we will first try to load a schema
with the file name "default.php".  This file should never be included with a theme.  If it
is, merge conflicts will occur as people update their code.  Rather, this should be defined
by administrators on a site by site basis.
default.php and default.css MUST be symlinks to existing scheme files.

You schema does not need to - and should not - contain all of these values.  Only the values
that differ from the defaults should be listed.  This gives you some very powerful options
with very few lines of code.

Note the options available differ with each theme.  The options available with the Redbasic 
theme are as follows:

* nav_colour
	The colour of the navigation bar.  Options are red, black and silver.  Alternatively, 
	one can set $nav_bg_1, $nav_bg_2, $nav_bg_3 and $nav_bg_4 to provide gradient and
	hover effects.
* banner_colour
	The font colour of the banner element.  Accepts an RGB or Hex value.
* bgcolour
	Set the body background colour.  Accepts an RGB or Hex value.
* background_image
	Sets a background image.  Accepts a URL or path.
* item_colour
	Set the background colour of items.  Accepts an RGB or Hex value.
* item_opacity
	Set the opacity of items.  Accepts a value from 0.01 to 1
* toolicon_colour
	Set the colour of tool icons.  Accepts an RGB or Hex value.
* toolicon_activecolour
	Set the colour of active or hovered icon tools.
* font_size
	Set the size of fonts in items and posts.  Accepts px or em.
* body_font_size
	Sets the size of fonts at the body level.  Accepts px or em.
* font_colour
	Sets the font colour.  Accepts an RGB or Hex value.
* radius
	Set the radius of corners.  Accepts a numeral, and is always in px.
* shadow
	Set the size of shadows shown with inline images.  Accepts a numerical 
	value.  Note shadows are not applied to smileys.
* converse_width
	Set the maximum width of the content region in px.
* nav_min_opacity
* top_photo
* reply_photo

If a your_schema_name.css file is found, the content of this file will be attached to the end of style.css.
This gives the schema developer the possibility to override any style component.



## Contributions

