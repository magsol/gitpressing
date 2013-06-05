# Wordpress Plugin: WordHub

This is a Wordpress plugin (forked from [this project](https://github.com/katzgrau/wordpress-github/) that will list your open source projects from github. You can have them inserted in a standard post or page, or have them inserted in your sidebar. It's in use at [magsol.me](http://www.magsol.me/projects).

In short, simply place:

`{{github:username,sortby:watchers,sortdir:desc}}`

in a post would pull your projects from github, merge them into one list, sort them in descending order by watchers, cache it, and place the list in your post. More below!

NOTE: Unlike the project from which this was forked, this supports *only github*. Support for bitbucket projects has been removed.

## Installation

Download a [zip](https://github.com/magsol/wordpress-github/zipball/master) extract it into `/wp-content/plugins/`. Rename the extracter folder to wordpress-github.

Should you should now have a `/wp-content/plugins/wordpress-github` directory.

Now log into the WP admin panel and activate the plugin. Go to the 'WordHub' settings page and do your thing (if you'd like, the plugin doesn't _need_ any configuration).

## Examples

### Insert in a page or post

Once you install the plug-in (see below), create a page (or open one) where you'd like your projects to be listed. On my personal website, this would be my '[Projects](http://www.magsol.me/projects)' page, which I was tired of updating :)

At the point where you'd like to insert your projects, put:

`{{github:your_username}}`

So for me, that was `{{github:magsol}}`.

### Insert in the sidebar (or some other widgety place)

This plugin also comes with a widget. Go to your Wordpress widgets page, and activate the 'WordHub' widget.

The 'Title' field is label for the widget listing. You might want to just put "Projects".

For 'Sources', put in a project string like: `github:your_username`. I use something like:

`github:magsol`

## Customization and Sorting

You can edit _how_ projects are listed on the settings page. Look for the 'WordHub' settings link in the Wordpress admin panel.

Customization options include formatting and sorting. For example, if you want projects with the most watchers listed first, do:

`{{github:username,sortby:watchers,sortdir:desc}`

You can also sort alphabetically:

`{{github:username,sortby:name,sortdir:asc}}`

Lastly, you can sort by the last update or push.

`{{github:username,sortby:updated,sortdir:desc}}`

## Other details

The plugin caches your projects for 1 hour. If you'd like to configure this,
 edit `WPGH_Core::$_cacheExpiration` in `wordhub.php`. This might be
 configurable via the admin interface later.

## License (Apache 2.0)

Copyright 2013 Shannon Quinn <magsol@gmail.com>

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.

All existing code retains its original authorship tags. Any new code will reflect its authorship.