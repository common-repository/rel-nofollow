=== Rel Nofollow ===
Contributors: Ste_95
Author URI: http://www.thecrowned.org
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=2WDRMXGHWCCUY
Tags: rel, links, seo
Tested up to: 6.6
Stable tag: 1.4
Requires at least: 3.7

Adds rel="nofollow" to posts external links unless specified otherwise.

== Description ==
When a post is saved, the plugin adds the rel="nofollow" attributes to post external links. The plugin also provides an apt checkbox to exclude a post from plugin's action.

Links which already have a *rel* attribute are just ignored, so you can set some *dofollow*s are well.

By default, the plugin will only act on *posts*, no pages or other custom post types. To include (some of) them, use a code like the following, for ex. by putting it in your theme's *functions.php*:

`add_filter( 'rnf_post_types', function( $post_types ) {
    return array( 'post', 'page' ); #specify all desired CPTs, comma-separated
});`

== Changelog ==
= 1.4 (2020/07/30) =
* Tweak: only include posts into plugin action (no pages or CPTs). To include other CPTs, see plugin description.

= 1.3 (2019/08/29) =
* Tweak: considering links as internal if on the same hostname (eg. if WP is installed in www.hostname.com/wordpress, even links pointing to www.hostname.com are internal).
* Fix: now adding rel nofollow even if a (different) rel attribute is already present, preserving it as well.

= 1.2 (2017/01/09) =
* Fix: plugin not ignoring links which already had the rel attribute.
* Tweak: bit of performance improvement.

= 1.1 (2016/05/21) =
* New: adding the nofollow only to external links.
* Tweak: declaring as static some class methods.

= 1.0 =
Initial release
