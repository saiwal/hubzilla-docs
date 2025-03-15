# Database updates

In the https://huburl/admin/dbsync page the administrator can check if any update was not successful and, if so, retry it.

If an update has failed but doesn't register as failed for some reason, the administrator can attempt to re-execute the update. For example for DB update #1999, by visiting the webpage:

https://huburl/admin/dbsync/1999


## Database Tables

| Table                                                                 | Description                                                          |
|----------------------------------------------------------------------|----------------------------------------------------------------------|
| [abconfig](db_abconfig.md)                      | arbitrary storage for connections of local channels                  |
| [abook](db_abook.md)                            | connections of local channels                                        |
| [account](db_account.md)                        | service provider account                                             |
| [addon](db_addon.md)                            | registered plugins                                                   |
| [app](db_app.md)                                | personal app data                                                    |
| [attach](db_attach.md)                          | file attachments                                                     |
| [auth_codes](db_auth_codes.md)                  | OAuth usage                                                          |
| [cache](db_cache.md)                            | OEmbed cache                                                         |
| [cal](db_cal.md)                                | CalDAV containers for events                                         |
| [channel](db_channel.md)                        | local channels                                                       |
| [chat](db_chat.md)                              | chat room content                                                    |
| [chatpresence](db_chatpresence.md)              | channel presence information for chat                                |
| [chatroom](db_chatroom.md)                      | data for the actual chat room                                        |
| [clients](db_clients.md)                        | OAuth usage                                                          |
| [config](db_config.md)                          | main configuration storage                                           |
| [conv](db_conv.md)                              | Diaspora private messages meta conversation structure                |
| [event](db_event.md)                            | Events                                                               |
| [pgrp_member](db_pgrp_member)                | privacy groups (collections.md), group info                             |
| [pgrp](db_pgrp)                              | privacy groups (collections.md), member info                            |
| [hook](db_hook.md)                              | plugin hook registry                                                 |
| [hubloc](db_hubloc.md)                          | xchan location storage, ties a hub location to an xchan              |
| [iconfig](db_iconfig.md)                        | extensible arbitrary storage for items                               |
| [issue](db_issue.md)                            | future bug/issue database                                            |
| [item](db_item.md)                              | all posts and webpages                                               |
| [item_id](db_item_id.md)                        | (deprecated by iconfig) other identifiers on other services for posts|
| [likes](db_likes.md)                            | likes of 'things'                                                    |
| [mail](db_mail.md)                              | private messages                                                     |
| [menu](db_menu.md)                              | webpage menu data                                                    |
| [menu_item](db_menu_item.md)                    | entries for webpage menus                                            |
| [notify](db_notify.md)                          | notifications                                                        |
| [obj](db_obj.md)                                | object data for things (x has y)                                     |
| [outq](db_outq.md)                              | output queue                                                         |
| [pconfig](db_pconfig.md)                        | personal (per channel) configuration storage                         |
| [photo](db_photo.md)                            | photo storage                                                        |
| [poll](db_poll.md)                              | data for polls                                                       |
| [poll_elm](db_poll_elm.md)                      | data for poll elements                                               |
| [profdef](db_profdef.md)                        | custom profile field definitions                                     |
| [profext](db_profext.md)                        | custom profile field data                                            |
| [profile](db_profile.md)                        | channel profiles                                                     |
| [profile_check](db_profile_check.md)            | DFRN remote auth use, may be obsolete                                |
| [register](db_register.md)                      | registrations requiring admin approval                               |
| [session](db_session.md)                        | web session storage                                                  |
| [shares](db_shares.md)                          | shared item information                                              |
| [sign](db_sign.md)                              | Diaspora signatures. To be phased out.                               |
| [site](db_site.md)                              | site table to find directory peers                                   |
| [source](db_source.md)                          | channel sources data                                                 |
| [sys_perms](db_sys_perms.md)                    | extensible permissions for OAuth                                     |
| [term](db_term.md)                              | item taxonomy (categories, tags, etc.) table                         |
| [tokens](db_tokens.md)                          | OAuth usage                                                          |
| [updates](db_updates.md)                        | directory sync updates                                               |
| [verify](db_verify.md)                          | general purpose verification structure                               |
| [vote](db_vote.md)                              | vote data for polls                                                  |
| [xchan](db_xchan.md)                            | list of known channels in the universe                               |
| [xchat](db_xchat.md)                            | bookmarked chat rooms                                                |
| [xconfig](db_xconfig.md)                        | as pconfig but for channels with no local account                    |
| [xign](db_xign.md)                              | channels ignored by friend suggestions                               |
| [xlink](db_xlink.md)                            | "friends of friends" linkages derived from poco, also ratings storage|
| [xperm](db_xperm.md)                            | OAuth/OpenID-Connect extensible permissions permissions storage      |
| [xprof](db_xprof.md)                            | if this hub is a directory server, contains basic public profile info of everybody in the network |
| [xtag](db_xtag.md)                              | if this hub is a directory server, contains tags or interests of everybody in the network        |
