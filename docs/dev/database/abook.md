# abook

| Field            | Description                                                                                  | Type              | Null | Key | Default             | Extra          |
|------------------|----------------------------------------------------------------------------------------------|-------------------|------|-----|---------------------|----------------|
| abook_id         | Sequential ID                                                                                | int(10) unsigned  | NO   | PRI | NULL                | auto_increment |
| abook_account    | account.account_id of the channel which owns this record                                     | int(10) unsigned  | NO   | MUL | NULL                |                |
| abook_channel    | channel.channel_id of the channel which owns this record                                     | int(10) unsigned  | NO   | MUL | NULL                |                |
| abook_xchan      | xchan.xchan_hash of the target identity (this channel's connection)                          | char(255)         | NO   | MUL |                     |                |
| abook_my_perms   | bitfield of all specific permissions granted this connection                                 | int(11)           | NO   | MUL | 0                   |                |
| abook_their_perms| bitfield of all permissions granted to you by this connection                                | int(11)           | NO   | MUL | 0                   |                |
| abook_closeness  | "closeness" value for optional affinity tool, 0-99                                           | tinyint(3) unsigned | NO   | MUL | 99                  |                |
| abook_created    | Datetime this record was created                                                             | datetime          | NO   | MUL | 0000-00-00 00:00:00 |                |
| abook_updated    | Datetime this record was modified                                                            | datetime          | NO   | MUL | 0000-00-00 00:00:00 |                |
| abook_connected  | datetime of last successful "poll" for this connection                                       | datetime          | NO   | MUL | 0000-00-00 00:00:00 |                |
| abook_dob        | Datetime of connection's birthday converted from *their* timezone to UTC                    | datetime          | NO   | MUL | 0000-00-00 00:00:00 |                |
| abook_flags      | No longer used                                                                               | int(11)           | NO   | MUL | 0                   |                |
| abook_profile    | profile.guid of profile to display to this connection if authenticated                       | char(64)          | NO   | MUL |                     |                |
| abook_blocked    | Bi-directional communications with this channel are blocked, regardless of other permissions | int(11)           | NO   | MUL | 0                   |                |
| abook_ignored    | Incoming communications from this channel are blocked, regardless of other permissions      | int(11)           | NO   | MUL | 0                   |                |
| abook_hidden     | This connection will not be shown as a connection to anybody but the channel owner          | int(11)           | NO   | MUL | 0                   |                |
| abook_archived   | This connection is likely non-functioning and the entry and conversations are preserved, but further polled communications will not be attempted | int(11) | NO   | MUL | 0                   |                |
| abook_pending    | A connection request was received from this channel but has not been approved by the channel owner, public communications may still be visible but no additional permissions have been granted | int(11) | NO   | MUL | 0                   |                |
| abook_unconnected| currently unused. Projected usage is to indicate "one-way" connections which were instigated on this end but are still pending on the remote end | int(11) | NO   | MUL | 0                   |                |
| abook_self       | is a special case where the owner is the target. Every channel has one abook entry with abook_self and with a target abook_xchan set to channel.channel_hash. When this flag is present, abook_my_perms is the default permissions granted to all new connections and several other fields are unused | int(11) | NO   | MUL | 0                   |                |
| abook_feed       | indicates this connection is an RSS/Atom feed and may trigger special handling               | int(11)           | NO   | MUL | 0                   |                |
| abook_incl       | connection filter allow rules separated by LF                                                | text              | NO   | MUL | 0                   |                |
| abook_excl       | connection filter deny rules separated by LF                                                 | text              | NO   | MUL | 0                   |                |
| abook_instance   | comma separated list of site urls of all channel clones that this connection is connected with (used only for singleton networks which don't support cloning) | text | NO   | MUL | 0                   |                |
