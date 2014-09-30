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

FTP
========================
- Neil and Phil have full access to FTP
- Additional FTP users can be created in the Bluehost cPanel
- Wordpress stuff is pretty stock.
- The first public facing folder is "*ftp://public_html/portal/*" which resolves at http://portal.clevelandfoodbank.org/yourfilehere.pdf
	- Poke around in this folder and you will find a few directories of manually uploaded stuff. 
- Theme stuff is found here: "*ftp://public_html/portal/wp-content/themes/*" 
- Plugin stuff is fund here: "*ftp://public_html/portal/wp-content/plugins/*"
- Uploaded files (manual through the GUI and through plugins) are found here: "*ftp://public_html/portal/wp-content/uploads/*"


Our Theme
========================
- Our theme is pretty heavily modified copy of [Support Desk](http://themeforest.net/theme_previews/4321280-support-desk-a-responsive-helpdesk-theme?url_name=support-desk-a-responsive-helpdesk-theme). 
- It has been forked to allow some hard coded changes to the Programs Portal. 
- The entire portal install uses "supportdesk" as it theme except for the programs portal which uses "supportdesk-programs".
- These are hosted on Github and can be used to restored via FTP if someone screws something up.  
	- Here is the Main Theme: https://github.com/philtrimble/GCFB-Portal-Theme---Main
	- Here is the Programs Theme: https://github.com/philtrimble/GCFB-Portal-Theme---Programs

Users
========================
- Wordpress has several different user permission levels. Neil and Phil are both superadmins who can do all kind of crazy stuff. 
- Regular users can be added by visiting http://portal.clevelandfoodbank.org/register and filling out the form.
    - There is currently no waitlist or approval process for new users. They are instantly created. This list should be monitored for Spam bots.
- Phil/Neil can both elevate other users to higher ranks as needed. Most internal staff can be made Editors of the site they need to edit/add content for. 

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

Repeted Manual Tasks and Maintainence
=========================
- At the end of each month a new month option should be added to the "Monthly Statistics" form on the agency portal. The oldest month on the list should be removed.
- New menus should be uploaded every quarter for the CFK. These are in a folder on the shared drive but should be double checked with Fatima
- Kids Cafe: Carli Nelson manages this section pretty independently. 
- Board Portal: The board packet files should be uploaded in a group via the file manager plugin. Phil and neil are both familiar with this process.
- The complete task list in Zapier should be checked for any errors: [CLICK HERE](https://zapier.com/goto/?payload=.eJxNjkEKwjAQRa8iA3ZVjBYKEgjioucoYzq00UwTkslCi3fX1o3b9z68v8CAgqAXEOLoUaifkQk0UEohZYWeksC7BqaccVxNx-i83lnv7ANq8G5-fOkkErNW6oXRUTrYwApjVJPLEtLzEm53stK7wZzb9tS0VRaUks2WqYpwn0NJlv4A0-AKG1pzG7DIEd04m27d7Jvj9XfuAwdQRxU:1XZ2Up:keBdLw2VGzHg7YL51_76aqoD89I)

Automated Tasks
=========================
- The menu uploads automatically to FTP via a Jet report that is sent up via a .bat file that Neil has running in the server room. This runs at 9:50am, 1:00pm, and 5:00pm.

Plugins
=========================
Plugins allow Wordpress to do a ton of extra stuff and we use a lot of them! Plugins are managed/installed/uninstalled/updated in the Network Admin section acessable by Phil/Neil/other Superusers. 
- **PLEASE NOTE** take great care when updating plugins as many conflicts can occur. Be diligent and read the release notes in full!

Gravity Forms
-------------------------
Gravity Forms is easily our most used plugin. It 


Gravity Forms has some of it's own plugins which are managed in the Network Admin Plugin's Panel:
- **GP Limit Choices**
- **Gravity Forms CSS Ready Class Selector** - Adds a GUI CSS picker in the Advanced tab of a field 
- **Gravity Forms Digest Bulk Reports** - Gemerates a email listing new responses to a form. Responses arrive in a .csv attachement. Used for grocery rescue.
- **Gravity Forms Saved Forms Add-On** - Allows a signed in user to save a form for a later session. Tested but not implemented. Google docs may be a better solution for local backup.
- **Gravity Forms User Registration Add-On** - Powers the end user registration form for creating a new account. Maps agency name to 'User_Description' in the user profile.
- **Gravity Forms Zapier Add-on** - Allows GF data to push to Zapier (See Zapier section)
- **Gravity Perks** - Small suite of GF tweaks from David Smith
- **GP Limit Choices** - Included in Gravity Perks. Allows radio buttons to hide based up number of times selected

S2 Member
-------------------------
- S2 Member manages user permissions on the front end of the site. 
- The permission levels are as follows:

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
To learn more about any of these plugins look them up here: https://wordpress.org/plugins/

- **Add Multiple Users** - *Allows for bulk import of numerous users. We haven't really used this since the big initial  import* 
- **Auto ThickBox Plus** - *Allows for lightboxed video pop overs of self hosted video*
- **bbPress** - *This is the backend for the forum section on each portal site. None are being used right now*
- **Easy Google Fonts** - *This allows for site wide use of the Karla font*
- **Featured Video Plus** - *Allows video headers in news stories*
- **Google Analytics** - *Talks to google analytics without the need for header injection*
- **Insert PHP Code Snippet** - *Allows direct use of PHP code within the editor through shortcodes (instead of hard codeding directly into the template). Currently used with "News-Ticker"*
- **Multisite Robots.txt Manager | MS Robots.txt** - *Search engine crawler blacklist used to keep search engines from indexing the portal*
- **News-Ticker** - *JS based ticker used on the main page of the Agency Portal. Requires "Insert PHP Code Snippet*
- **NS Cloner - Site Copier** - *Used to make copies of a multi-site instance.*
- **Responsive Lightbox** - *Image lightbox for posts/pages. May be able to be depricated when WP instal is updated*
- **Reveal IDs** - *Shows page/post IDs in the backend list*
- **Search & Replace** - *Allows minor DB edits without having to jump into PHPmyAdmin. Use with caution.*
- **Secure HTML5 Video Player** - *Allows streaming of selfhosted .mp4 filies within pages/posts*
- **Simple Local Avatars** - *Allows use of user avatars without the need for the Gravatars service*
- **Simple Network Login Log** - *Logs user logins*
- **Snapshot** - *Create ad hoc backups before trying something crazy*
- **Substitute Displayname** - *Applies "FirstName, LastName - AgencyName" for all news users site wide.*
- **Ultimate Branding** - *Strips out a bunch of wordpress cruft*
- **User Activity**
- **User Switching** - *Allows super admin to assume the role of a logged in user. Great for supplying a new plaintext password to a novice user*
- **WordPress Admin Bar Improved** - *Cleans up the Admin Bar for users*
- **WordPress Pop Up Plugin** - *Allows text popovers. Currently used on the Kids Cafe page*
- **WP Smush.it** - *Optimizes image uploads for web viewing*
- **WP Super Cache** - *Caches static page elements. Helps with load times. Don't fiddle with this too much - it's easy to really bring the site to a grinding halt.*

