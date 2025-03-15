# Database updates

In the https://huburl/admin/dbsync page the administrator can check if any update was not successful and, if so, retry it.

If an update has failed but doesn't register as failed for some reason, the administrator can attempt to re-execute the update. For example for DB update #1999, by visiting the webpage:

https://huburl/admin/dbsync/1999


## Database Tables

| Table                                                                 | Description                                                          |
|----------------------------------------------------------------------|----------------------------------------------------------------------|
| [abconfig](db_abconfig)                      | arbitrary storage for connections of local channels                  |
| [abook](db_abook)                            | connections of local channels                                        |
| [account](db_account)                        | service provider account                                             |
| [addon](db_addon)                            | registered plugins                                                   |
| [app](db_app)                                | personal app data                                                    |
| [attach](db_attach)                          | file attachments                                                     |
| [auth_codes](db_auth_codes)                  | OAuth usage                                                          |
| [cache](db_cache)                            | OEmbed cache                                                         |
| [cal](db_cal)                                | CalDAV containers for events                                         |
| [channel](db_channel)                        | local channels                                                       |
| [chat](db_chat)                              | chat room content                                                    |
| [chatpresence](db_chatpresence)              | channel presence information for chat                                |
| [chatroom](db_chatroom)                      | data for the actual chat room                                        |
| [clients](db_clients)                        | OAuth usage                                                          |
| [config](db_config)                          | main configuration storage                                           |
| [conv](db_conv)                              | Diaspora private messages meta conversation structure                |
| [event](db_event)                            | Events                                                               |
| [pgrp_member](db_pgrp_member)                | privacy groups (collections), group info                             |
| [pgrp](db_pgrp)                              | privacy groups (collections), member info                            |
| [hook](db_hook)                              | plugin hook registry                                                 |
| [hubloc](db_hubloc)                          | xchan location storage, ties a hub location to an xchan              |
| [iconfig](db_iconfig)                        | extensible arbitrary storage for items                               |
| [issue](db_issue)                            | future bug/issue database                                            |
| [item](db_item)                              | all posts and webpages                                               |
| [item_id](db_item_id)                        | (deprecated by iconfig) other identifiers on other services for posts|
| [likes](db_likes)                            | likes of 'things'                                                    |
| [mail](db_mail)                              | private messages                                                     |
| [menu](db_menu)                              | webpage menu data                                                    |
| [menu_item](db_menu_item)                    | entries for webpage menus                                            |
| [notify](db_notify)                          | notifications                                                        |
| [obj](db_obj)                                | object data for things (x has y)                                     |
| [outq](db_outq)                              | output queue                                                         |
| [pconfig](db_pconfig)                        | personal (per channel) configuration storage                         |
| [photo](db_photo)                            | photo storage                                                        |
| [poll](db_poll)                              | data for polls                                                       |
| [poll_elm](db_poll_elm)                      | data for poll elements                                               |
| [profdef](db_profdef)                        | custom profile field definitions                                     |
| [profext](db_profext)                        | custom profile field data                                            |
| [profile](db_profile)                        | channel profiles                                                     |
| [profile_check](db_profile_check)            | DFRN remote auth use, may be obsolete                                |
| [register](db_register)                      | registrations requiring admin approval                               |
| [session](db_session)                        | web session storage                                                  |
| [shares](db_shares)                          | shared item information                                              |
| [sign](db_sign)                              | Diaspora signatures. To be phased out.                               |
| [site](db_site)                              | site table to find directory peers                                   |
| [source](db_source)                          | channel sources data                                                 |
| [sys_perms](db_sys_perms)                    | extensible permissions for OAuth                                     |
| [term](db_term)                              | item taxonomy (categories, tags, etc.) table                         |
| [tokens](db_tokens)                          | OAuth usage                                                          |
| [updates](db_updates)                        | directory sync updates                                               |
| [verify](db_verify)                          | general purpose verification structure                               |
| [vote](db_vote)                              | vote data for polls                                                  |
| [xchan](db_xchan)                            | list of known channels in the universe                               |
| [xchat](db_xchat)                            | bookmarked chat rooms                                                |
| [xconfig](db_xconfig)                        | as pconfig but for channels with no local account                    |
| [xign](db_xign)                              | channels ignored by friend suggestions                               |
| [xlink](db_xlink)                            | "friends of friends" linkages derived from poco, also ratings storage|
| [xperm](db_xperm)                            | OAuth/OpenID-Connect extensible permissions permissions storage      |
| [xprof](db_xprof)                            | if this hub is a directory server, contains basic public profile info of everybody in the network |
| [xtag](db_xtag)                              | if this hub is a directory server, contains tags or interests of everybody in the network        |
