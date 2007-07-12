=== Naatan.com Useronline v2.0.2 ===
Contributors: Naatan
Donate link: http://www.naatan.com/
Tags: user online, useronline, users online, online, users, statistics
Requires at least: 2.x
Tested up to: 2.1
Stable tag: trunk

Adds A Useronline Feature To WordPress featuring user names and search bot detection.

== Description ==

Adds A Useronline Feature To WordPress featuring user names and search bot detection. Supports widgets and comes with configuration page.

NEW IN 2.0

    * 2.0.2 Update: Fixed widget option not showing up.
    * 2.0.2 Update: Fixed MySQL error "Duplicate entry '32767' for key 1" Fixed.
    * 2.0.1 Update: Fixed bug where only one user at a time could be monitored.

    * Added: Widget Support
    * Added: Search Bot detection
    * Added: Custom Names feature
      This feature enables you to add tags to custom user names such as your own, 
      enabling you to change for example the text color for every person that visits your blog.
    * Added: Configuration Panel
    * Improved: Functionality
      Users are now first checked on IP, then on cookie. Also users are now checked for a 
      registration cookie aswell, so you don’t have to logout and comment on your own blog to enable it anymore ;)
    * Fixed: Several bugs, for example, names would never show up with a link, this issue is now resolved.

== Installation ==

   1. Upload “naatan_useronline.php” to your plugins directory
   2. Enable the plugin in WP Plugin Management
   3. That’s it!

UPDATE INSTRUCTIONS

   1. Simply replace your old “naatan_useronline.php” with the new one.
   2. NOTE That you WILL have to change your useronline templates if your updating from 1.x!
      Previous version already used the echo command in the function itself, this is changed in the new version!
      Check the FUNCTION USAGE section for more info on this, I would recommend using the template on this page and customize it for yourself.

== Arbitrary section ==

Usage with Wordpress Widgets

   1. Just enable it like any other widget plugin


Usage WITHOUT Wordpress Widgets

   1. Open your sidebar template (or any other template you want to place it in)
   2. Add the following where you want it;

      There are currently <b><?php echo naatan_useronlinecount(); ?></b> users online.<br>
      <?php echo naatan_namedbits(); ?><i><b><?php echo naatan_guestonlinecount(); ?></b> Guest(s), <b><?php echo naatan_botonlinecount(); ?></b> Bot(s)</i>

   3. Save the template and your done! Naturally you can customize this however you want.

== A brief Markdown Example ==

SCRIPT FUNCTIONS

    * naatan_useronlinecount - Returns the number of total online users
    * naatan_namedonlinecount - Returns the number of named online users
    * naatan_guestonlinecount - Returns the number of unnamed online users
    * naatan_botonlinecount - Returns the number of search bots currently on your site
    * naatan_namedbits - Returns a list (seperated by comma’s) of the named online users

FUNCTION USAGE

Every function can be called as any other WP function, for example;

<?php echo naatan_namedbits(); ?>

and another example;

<?php echo naatan_useronlinecount(); ?<

Note that the previous version did not use echo.
