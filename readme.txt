  ___  _     _                         
 / _ \| |   | |                        
/ /_\ \ |__ | | _____  _ __  ___ _   _ 
|  _  | '_ \| |/ / _ \| '_ \/ __| | | |
| | | | | | |   < (_) | | | \__ \ |_| |
\_| |_/_| |_|_|\_\___/|_| |_|___/\__,_|
                                       
                                      
        
        \||/
                |  @___oo
      /\  /\   / (__,,,,|
     ) /^\) ^\/ _)
     )   /^\/   _)
     )   _ /  / _)
 /\  )/\/ ||  | )_)
<  >      |(,,) )__)
 ||      /    \)___)\
 | \____(      )___) )___
  \______(_______;;; __;;;
  
   
/*
Plugin Name: WPProAtoZ Mobile Call Now & Map Buttons
Plugin URI: https://wpproatoz.com
Description: Adds a quick call button and map access to mobile phone for you users to be able to get quick instructions and or call you. Adds custom "Call Now" and/or Google Map "Directions" buttons for mobile visitors. Forked from davidsworld plugin
Version: 1.5.1
Requires at least: 6.0
Requires PHP: 8.0
Tested up to: 6.8.1
Author: WPProAtoZ.com
Author URI: https://wpproatoz.com
Text Domain: wpproatoz-quickmobile-call-map-buttons
Update URI: https://github.com/Ahkonsu/wpproatoz-quickmobile-call-map-buttons/releases
GitHub Plugin URI: https://github.com/Ahkonsu/wpproatoz-quickmobile-call-map-buttons/releases
GitHub Branch: main
Tags: mobile, cell, responsive, buttons, phone, call, contact, map, location, directions, customize, call us, phone now, get directions
License: GPLv3
Contributors: davidsword, vklakkineni
*/

== Description ==

= Adds "Call Now" and "Directions" buttons on devices =

* Easily customize the bar, the text, buttons colors font
* Set which device size range the buttons will appear for

= Please Note =

* This is a forked plugin,** recently revived after it was abobnded on the wp repo Fork of the Mobile Call Now and Map Buttons plugin Adds custom "Call Now" and/or Google Map "Directions" buttons for mobile visitors.


---

== Installation ==

1. Upload the plugin files to the `/wp-content/plugins/mobile-call-now-map-buttons` directory, or install the plugin through the WordPress plugins screen directly.
2. Activate the plugin through the 'Plugins' screen in WordPress
3. Use the 'Settings > Mobile Call Now & Map Buttons' page to configure the plugin


== Frequently Asked Questions ==

= How is the maps button created? =

The address is built with a Google Maps URL query. Your entered location (address or GPS coord) values are constructed into a link like so:

`https://maps.google.com/?q=( street, city, province/state, country, postal/zip or latitude,longitude)`

If you're having troubles with your address, please be sure your business listing is correct on [google.com/maps](https://google.com/maps/) first, or use the GPS Coordinates option in the plugin.

If your *google.com/maps/* listing is incorrect, don't hesitate talking to Google about it, in our experience, they're eager to resolve map issues.


= What Format For GPS Coordinates? =

Please use the decimal degrees format (`dd.ddddd`) for GPS coordinates. Do not enter the degree symbol or N/E/S/W direction mention or commas. For example, Kamloops BC Canada would be:

*Latitude:* `50.6745`
*Longitude:* `-120.3273`


= The buttons are hiding my footer =

This should not happen, but is due to a CSS conflict between the plugin and your theme. 


= The buttons are appearing above lightbox / popups =

See **z-index** below.


= Advanced Options: z-index =

Absolute positioned elements on websites can be layered on top of one another using the CSS property `z-index`. This plugin has the buttons on a `z-index` of `998`. It's at this number as most popup's and lightbox's use `999` or higher.

If your theme has something hidden behind the buttons, or the buttons are above something like Lightbox, try altering this number higher or lower.

= Advanced Options: Append to body =

This plugin puts it’s HTML at the bottom of a page using Wordpress's `wp_footer` hook. As specified by WordPress:

> the `wp_footer` action. Put this template tag immediately before `</body>` tag in a theme template

Some theme authors, for whatever their reason, ignore this, wrapping `wp_footer()` in a few elements, causing problems for plugins like this that expect it in a certain place.

Selecting the **Move plugin to absolute bottom** option, Javascript will edit the DOM and move the plugin to be at the absolute bottom of your theme, regardless of where the Theme author placed wp_footer hook.


= Advanced Options: Number Sanitizing =

Select this option to prevent the plugin from re-formatting your phone number. By default if you enter a value like

`1 (555) 555 - 5555`

For maximum browser compatibility, the plugin will sanitize the phone number to

`1-555-555-5555`

This sometimes effects Google Adwords phone numbers that expect a certain phone number format.


= Advanced Options: Profile =

This is your Wordpress setup, you may copy/paste it out when needing help troubleshooting your site.


== Screenshots ==

1. Settings page
2. Out of the box settings on Twenty Fifteen on iPhone 6s emulator
3. Alt settings on Twenty Fifteen on iPhone 6s emulator


== Road Map ==

= The todo list: =

* verify: compatibility with typeform.com
* add: Google API address results in backend for auto-filling
* add: a Google Universal Analytics support
* add: Set a button to link to a page or url
* feature you'd like to see? 

== Changelog ==
= 1.5.1 =
* July 25, 2025
* updated code to be complatble with php 8+ fixed error for depreciated property

= 1.5.0 =
* Mar 5, 2018
* readme and doc change
* added php version requirement

= 1.4.2 =
* Jan 24, 2018
* minor change to init

= 1.4.1 =
* Jan 24, 2018
* Fixed CSS where when one-button use would result in off-center button (thanks Z.J.!)
* added security measure for direct file access (`if !defined(ABSPATH) exit`)

== Upgrade Notice ==

= 1.0.1 =

* All good.

= 1.0 =

* If any custom CSS was written for this plugin, note all front end CSS selectors have been changed to new shorter ones
= Inital Plugin Developed By =

* [David Sword](https://davidsword.ca/)
* [V. K. Lakkineni](https://lakkineni.com/)
