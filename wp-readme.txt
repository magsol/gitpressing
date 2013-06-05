=== Plugin Name ===
Contributors: Shannon Quinn
Tags: github,projects,project,list
Requires at least: 3.0
Tested up to: 3.3.2
Stable tag: 0.2

This is a Wordpress plugin that will list your open source projects from github in-page or via sidebar.

== Description ==

This is a Wordpress plugin that will list your open source projects from github. You can have them inserted in a standard post or page, or have them inserted in your sidebar. It's in use at [magsol.me](http://www.magsol.me/projects).

So in short, just placing:

    {{github:username,sortby:watchers,sortdir:desc}}

in a post would pull your projects from github, merge them into one list, sort them in descending order by w atchers, cache it, and place the list in your post. More detail at [the github repository](https://github.com/magsol/wordpress-github).

The plugin also comes packaged with a widget in case you'd just like to list your projects in the sidebar. Full details are on the settings page.

== Installation ==

There aren't really any special instructions for installing this plug-in. Once installed, be sure to go to the GitPressing settings page if you'd like to customize your template.
