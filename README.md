Introduction
====================
The portal is built on Wordpress (http://wordpress.org), a free, mature, and open CMS built with PHP on a SQL database. This is currently running in a multisite environment comprised of five sites:

1. *Main Landing Page* (http://portal.clevelandfoodbank.org/)
2. *Agency Portal* (http://portal.clevelandfoodbank.org/agency/)
3. *Programs Portal* (http://portal.clevelandfoodbank.org/programs/)
4. *Board Portal* (http://portal.clevelandfoodbank.org/board/)
5. *Employee Landing Page* (for the breakroom) (http://portal.clevelandfoodbank.org/employee/)

Hosting
=========================
- Our webhost is Bluehost (http://bluehost.com). We have a shared hosting plan, which has scaled well so far. 
- Neil and Phil have the account into for our hosting account and can access the cPanel. Hard coded DB edits can be done through PHPmyadmin in the cPanel. 
- You can check Bluehost's status by visiting their status page: (https://www.bluehost.com/cgi/serverstatus/) or twitter: (https://twitter.com/bluehostsupport)

General Wordpress Usage
=========================
###Posts
- Posts are the regular blog entries you write that appear on your home page. You write posts by clicking the Write tab. By default, the Posts subtab is selected. Complete the fields and information, select or create a category, and then click the Publish button.
- If you are creating a post on the Agency or Programs portal choose "Level 0" from the S2Member drop down on the right hand side bar at the top.
- Lost? Look here: (http://codex.wordpress.org/WordPress_Quick_Start_Guide#Create_Content)

###Pages
- Pages work just like Posts and should be configured the same way. Click on Pages in the backend to get started. There are a few additonal things to do.
  - Set the sidebar option as "none". This is not done by default. This option is found below body field in the "Page Options" section.
  - (Optional) Choose if the new page has a parent. This puts its a level deeper in the page heirarchy. Example: if the page is titled "Downloads" and the "Event" is choosen as the parent the URL would be http://portal.clevelandfoodbank.org/event/downloads/ 
  - (Optional) You can change the URL of your page by putting a value in the slug field at the bottom of the page. This will override the long/sloppy URL that a page titled "2014 Agency Awards Luncheon" would yield.
  - - Lost? Look here: (http://codex.wordpress.org/WordPress_Quick_Start_Guide#Create_Content)

###Calendar
- Events are handled by a plugin aptly named "The Events Calendar" which is developed by Modern Tribe. Click "New Event" to get started. 
- Events begin just like creating a post or page. Below the body of the event are additional options to configure related to time/place. Fill these out. 
- Additionally, you can choose a category for your event from the menu in the right side bar. This will apply a label and color to the event on the main calendar. 
- Lost? Here's a bunch of extra info: (http://tri.be/support/faqs/) 


Gravity Forms
=========================

S2 Member
=========================


