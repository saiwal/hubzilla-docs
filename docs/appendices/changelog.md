# Changelog 

* Cleanup deprecated forum queries, improved performance
* Fix zot6 handler returning success allthough Libzot::fetch() did not return anything useful
* Fix json encoding of a possibly empty item.target
* Fix permalink for forum posts and comments
* Fix an obscure delivering issue which could produce duplicate posts
* Lazy load profile photos for reactions to reduce server load
* Pubcrawl: deal with Update(Tombstone)
* Pubcrawl: fix mentions not mapped to "to" in public toplevel posts (regression)

