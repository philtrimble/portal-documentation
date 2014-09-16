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
- Bluehost does nightly backups of FTP and the DB which can be rolled back in case of emergency. This should be done with extreme care and will not restore DB changes occuring after the last nightly backup. More info here: https://my.bluehost.com/cgi/help/719
- You can check Bluehost's status by visiting their 
    - status page: (https://www.bluehost.com/cgi/serverstatus/) 
    - or twitter: (https://twitter.com/bluehostsupport)

Users
========================
- Wordpress has several different user permission levels. Neil and Phil are both superusers who can do all kind of crazy stuff. 
- Regular users can be added by visiting http://portal.clevelandfoodbank.org/register and filling out the form.
    - There is currently no waitlist or approval process for new users. They are instantly created. This list should be monitored for Spam bots.
- Phil/Neil can both elevate other users to higher ranks as needed. 

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

Plugins
=========================
Plugins allow Wordpress to do a ton of extra stuff and we use a lot of them! Plugins are managed/installed/uninstalled/updated in the Network Admin section acessable by Phil/Neil/other Superusers. 
- **PLEASE NOTE** take great care when updating plugins as many conflicts can occur. Be diligent and read the release notes in full!

Gravity Forms
-------------------------

Gravity Forms has some of it's own plugins which are managed in the Network Admin Plugin's Panel:
- **GP Limit Choices**
- **Gravity Forms CSS Ready Class Selector**
- **Gravity Forms Digest Bulk Reports**
- **Gravity Forms Saved Forms Add-On**
- **Gravity Forms User Registration Add-On**
- **Gravity Forms Zapier Add-on**
- **Gravity Perks**
- **GP Limit Choices**

S2 Member
-------------------------

LearnDash LMS
-------------------------

The Events Calendar / The Events Calendar PRO
-------------------------
Add-on Plugin: 
- **The Events Calendar Category Colors**

TablePress
-------------------------


Misc Plugins
-------------------------
- **Add Multiple Users** - *Allows for bulk import of numerous users. We haven't really used this since the big initial  import* 
- **Auto ThickBox Plus**
- **bbPress**
- **Easy Google Fonts**
- **Featured Video Plus**
- **Google Analytics**
- **Insert PHP Code Snippet**
- **Multisite Robots.txt Manager | MS Robots.txt**
- **News-Ticker**
- **NS Cloner - Site Copier**
- **Responsive Lightbox**
- **Reveal IDs**
- **Search & Replace**
- **Secure HTML5 Video Player**
- **Simple Local Avatars**
- **Simple Network Login Log**
- **Snapshot**
- **Substitute Displayname**
- **Ultimate Branding**
- **User Activity**
- **User Switching**
- **WordPress Admin Bar Improved**
- **WordPress Pop Up Plugin**
- **WP Smush.it**
- **WP Super Cache**

