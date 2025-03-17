# Database updates

In the https://huburl/admin/dbsync page the administrator can check if any update was not successful and, if so, retry it.

If an update has failed but doesn't register as failed for some reason, the administrator can attempt to re-execute the update. For example for DB update #1999, by visiting the webpage:

https://huburl/admin/dbsync/1999


## Database Tables

| Table                                                                 | Description                                                          |
|----------------------------------------------------------------------|----------------------------------------------------------------------|
| [abconfig](abconfig.md)                      | arbitrary storage for connections of local channels                  |
| [abook](abook.md)                            | connections of local channels                                        |
| [account](account.md)                        | service provider account                                             |
| [addon](addon.md)                            | registered plugins                                                   |
| [app](app.md)                                | personal app data                                                    |
| [attach](attach.md)                          | file attachments                                                     |
| [auth_codes](auth_codes.md)                  | OAuth usage                                                          |
| [cache](cache.md)                            | OEmbed cache                                                         |
| [cal](cal.md)                                | CalDAV containers for events                                         |
| [channel](channel.md)                        | local channels                                                       |
| [chat](chat.md)                              | chat room content                                                    |
| [chatpresence](chatpresence.md)              | channel presence information for chat                                |
| [chatroom](chatroom.md)                      | data for the actual chat room                                        |
| [clients](clients.md)                        | OAuth usage                                                          |
| [config](config.md)                          | main configuration storage                                           |
| [conv](conv.md)                              | Diaspora private messages meta conversation structure                |
| [event](event.md)                            | Events                                                               |
| [pgrp_member](pgrp_member.md)                | privacy groups (collections.md), group info                             |
| [pgrp](pgrp.md)                              | privacy groups (collections.md), member info                            |
| [hook](hook.md)                              | plugin hook registry                                                 |
| [hubloc](hubloc.md)                          | xchan location storage, ties a hub location to an xchan              |
| [iconfig](iconfig.md)                        | extensible arbitrary storage for items                               |
| [issue](issue.md)                            | future bug/issue database                                            |
| [item](item.md)                              | all posts and webpages                                               |
| [item_id](item_id.md)                        | (deprecated by iconfig) other identifiers on other services for posts|
| [likes](likes.md)                            | likes of 'things'                                                    |
| [mail](mail.md)                              | private messages                                                     |
| [menu](menu.md)                              | webpage menu data                                                    |
| [menu_item](menu_item.md)                    | entries for webpage menus                                            |
| [notify](notify.md)                          | notifications                                                        |
| [obj](obj.md)                                | object data for things (x has y)                                     |
| [outq](outq.md)                              | output queue                                                         |
| [pconfig](pconfig.md)                        | personal (per channel) configuration storage                         |
| [photo](photo.md)                            | photo storage                                                        |
| [poll](poll.md)                              | data for polls                                                       |
| [poll_elm](poll_elm.md)                      | data for poll elements                                               |
| [profdef](profdef.md)                        | custom profile field definitions                                     |
| [profext](profext.md)                        | custom profile field data                                            |
| [profile](profile.md)                        | channel profiles                                                     |
| [profile_check](profile_check.md)            | DFRN remote auth use, may be obsolete                                |
| [register](register.md)                      | registrations requiring admin approval                               |
| [session](session.md)                        | web session storage                                                  |
| [shares](shares.md)                          | shared item information                                              |
| [sign](sign.md)                              | Diaspora signatures. To be phased out.                               |
| [site](site.md)                              | site table to find directory peers                                   |
| [source](source.md)                          | channel sources data                                                 |
| [sys_perms](sys_perms.md)                    | extensible permissions for OAuth                                     |
| [term](term.md)                              | item taxonomy (categories, tags, etc.) table                         |
| [tokens](tokens.md)                          | OAuth usage                                                          |
| [updates](updates.md)                        | directory sync updates                                               |
| [verify](verify.md)                          | general purpose verification structure                               |
| [vote](vote.md)                              | vote data for polls                                                  |
| [xchan](xchan.md)                            | list of known channels in the universe                               |
| [xchat](xchat.md)                            | bookmarked chat rooms                                                |
| [xconfig](xconfig.md)                        | as pconfig but for channels with no local account                    |
| [xign](xign.md)                              | channels ignored by friend suggestions                               |
| [xlink](xlink.md)                            | "friends of friends" linkages derived from poco, also ratings storage|
| [xperm](xperm.md)                            | OAuth/OpenID-Connect extensible permissions permissions storage      |
| [xprof](xprof.md)                            | if this hub is a directory server, contains basic public profile info of everybody in the network |
| [xtag](xtag.md)                              | if this hub is a directory server, contains tags or interests of everybody in the network        |
