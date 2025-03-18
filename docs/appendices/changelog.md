# Changelog

## Release notes

* Allow to send signed requests from the zot_probe tool
* Print an error message if OWA fails
* Remove possible leading @ before processing webfinger address
* Updated debian install script
* Calculate observer.baseurl from xchan_url instead of xchan_connurl
* Refactor unparse_url() to allow return of a custom field set only and add tests
* Slightly improve event object rendering
* Update smarty library to version 5 for PHP 8.4 compatibility
* Remove vendor/symfony from gitignore file
* Update composer libraries
* Add contextHistory field to activities and prefer it over context when consuming
* Implement highlight button in jot editor
* Add test results and PHPStan to gitignore
* Update spanish strings
* Remove EpubMeta library in favor of a custom solution
* Configue gd for jpeg support in CI
* Add error message on missing owa auth headers
* Add Zotlabs\Tests namespace to autloader in dev
* Add dba_pdo::update method
* Add dba_pdo::insert method
* Rewrite redbasic javascript to remove jquery dependency
* Add security policy SECURITY.md

## Bugfixes

* Fix notifications for likes on our comments
* Fix fullscreen view
* Fix boxy scheme text alignment for comments
* Fix poll date string to match with the autotime string
* Fix owner hash not set correctly when editing a post/comment
* Fix an issue where some participants could not post to forums
* Fix navbar selector conflict with possible additional navbars when using a cover photo
* Fix target and tgt_type not set for sourced rss items if we rewrite them to our own
* Fix auto save draft not set correctly
* Fix cover height calculation

## Addons

* Diaspora: revisit import_diaspora_account()
* Pubcrawl: escape quotation marks in ActivityStreams link header
* Wiki: fixed wiki_page_list.tpl to use bootstrap class for layout
* BBmath: fix orientation for inline math
* BBmath: document imagemagick permissions
* Pubcrawl: ensure we select the correct hubloc hash when extending recipients list
* Msg_footer: do not add footer on edit, also dismiss anything but a create activity
* Pubcrawl: refactor activitypub addressing
* Wiki: added space to preview panel
* Startpage: update help text and some cleanup
