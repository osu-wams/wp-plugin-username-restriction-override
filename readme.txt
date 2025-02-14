=== Network Username Restrictions Override ===
Contributors: joraff
Tags: admin, authentication, network, wpmu, multisite
Requires at least: 3.4
Tested up to: 4.4.2
Stable tag: 1.3.1

Override restrictions on WordPress network usernames.

Note: this is a fork of https://wordpress.org/plugins/network-username-restrictions-override/, which is not actively maintained.

== Description ==

By default, WordPress network usernames cannot contain anything but lowercase letters and numbers. This plugin adds network options to let you include hyphens, underscores, or uppercase letters, if desired.

Furthermore, this plugin gives you the option to allow email addresses as usernames, or to allow all-numeric usernames (e.g. "1234").

Finally, this plugin lets you override the minimum length for usernames (which defaults to two characters).


== Installation ==

1. Login as a network admin and navigate to the Network Admin panel.
2. Upload the `network-username-restrictions-override` folder to your plugins folder, usually `wp-content/plugins`. (Or simply via the built-in installer.)
3. Network Activate the plugin on the Plugins screen.
4. Under Settings, enable any of the additional characters or formats for usernames.
5. Add new users via the Users menu.

== Frequently Asked Questions ==

= Why do my usernames end up in lowercase letters when I use uppercase? =

Unfortunately, the WordPress code for adding users forces usernames to lowercase without offering an option to configure it via a plugin.

= I have site URLs based on the username. Why don't some of them load? =

You'll have to update the regular expressions in your `.htaccess` file if you use email addresses or periods in site URLs. The default WordPress `.htaccess` configuration does not allow them, nor will this plugin edit your `.htaccess` automatically due to the risk involved.

== Screenshots ==

1. Plugin options

== Changelog ==
= 1.3.1 =
* Adding Composer information

= 1.3 =
* Fixes compatibility with PHP7.0
* Fixes compatibility with WordPress 4.4+

= 1.2 =
* Remove use of call-time pass by reference to avoid warnings on PHP 5.3 and newer
* Secondary username length check no longer causes an error when adding a username longer than the configured minimum
* Match error message with http://core.trac.wordpress.org/changeset/20441
* Add support for periods in usernames

= 1.1 =
* Update plugin URIs
* Add a check for super admins setting the minimum username length to longer than four characters

= 1.0 =
* Initial release
