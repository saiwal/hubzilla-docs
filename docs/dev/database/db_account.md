# account
| Field                    | Description                                                                                                                        | Type             | Null | Key | Default             | Extra          |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------- | ---- | --- | ------------------- | -------------- |
| account_id               | table index                                                                                                                        | int(10) unsigned | NO   | PRI | NULL                | auto_increment |
| account_parent           | for hierarchical accounts, the account_id of the parent to this one, if account_parent = account_id, this is the top level account | int(10) unsigned | NO   | MUL | 0                   |                |
| account_default_channel  | channel_id of channel to connect on login                                                                                          | int(10) unsigned | NO   | MUL | 0                   |                |
| account_salt             | complexity token for account_password                                                                                              | char(32)         | NO   |     |                     |                |
| account_password         | hashed password for this account                                                                                                   | char(255)        | NO   |     |                     |                |
| account_email            | essentially the login ID, although it is usually possible to login with a channel address                                          | char(255)        | NO   | MUL |                     |                |
| account_external         | Currently unused                                                                                                                   | char(255)        | NO   | MUL |                     |                |
| account_language         | default language (closest available browser-accept language when account was created)                                              | char(16)         | NO   |     | en                  |                |
| account_created          | timestamp of account creation                                                                                                      | datetime         | NO   |     | 0000-00-00 00:00:00 |                |
| account_lastlog          | timestamp of last login (or daily update if "remember me" is in effect)                                                            | datetime         | NO   | MUL | 0000-00-00 00:00:00 |                |
| account_flags            | see notes                                                                                                                          | int(10) unsigned | NO   | MUL | 0                   |                |
| account_roles            | see notes                                                                                                                          | int(10) unsigned | NO   | MUL | 0                   |                |
| account_reset            | verification token for password reset                                                                                              | char(255)        | NO   |     |                     |                |
| account_expires          | timestamp when account expires and will be deleted                                                                                 | datetime         | NO   | MUL | 0000-00-00 00:00:00 |                |
| account_expire_notified  | timestamp of last warning of account expiration                                                                                    | datetime         | NO   |     | 0000-00-00 00:00:00 |                |
| account_service_class    | service class for this account, determines what if any limits/restrictions are in place                                            | char(32)         | NO   | MUL |                     |                |
| account_level            | future use                                                                                                                         | int(10) unsigned | NO   | MUL | 0                   |                |
| account_password_changed | timestamp of last password change - to limit account deletion for 48 hours to prevent malicious activity                           | datetime         | NO   | MUL | 0000-00-00 00:00:00 |                |

## Notes:



### Account Flags

define ( 'ACCOUNT_OK',           0x0000 );
define ( 'ACCOUNT_UNVERIFIED',   0x0001 );
define ( 'ACCOUNT_BLOCKED',      0x0002 );
define ( 'ACCOUNT_EXPIRED',      0x0004 );
define ( 'ACCOUNT_REMOVED',      0x0008 );
define ( 'ACCOUNT_PENDING',      0x0010 );

### Account roles

define ( 'ACCOUNT_ROLE_SYSTEM',    0x0002 ); // 2 - this is the special system account
define ( 'ACCOUNT_ROLE_DEVELOPER', 0x0004 );
define ( 'ACCOUNT_ROLE_ADMIN',     0x1000 ); // 4096 - this account is an administrator


