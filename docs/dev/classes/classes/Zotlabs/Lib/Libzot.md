***

# Libzot





* Full name: `\Zotlabs\Lib\Libzot`




## Methods


### new_uid



```php
public static new_uid(string $channel_nick): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel_nick` | **string** | a unique nickname of controlling entity |





***

### make_xchan_hash



```php
public static make_xchan_hash(string $guid, string $pubkey): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$guid` | **string** |  |
| `$pubkey` | **string** |  |





***

### get_hublocs



```php
public static get_hublocs(string $hash): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hash` | **string** | - xchan_hash |


**Return Value:**

of hubloc (hub location structures)




***

### build_packet



```php
public static build_packet(array $channel, string $type = &#039;activity&#039;, array $recipients = null, array $msg = [], string $encoding = &#039;activitystreams&#039;, string $remote_key = null, string $methods = &#039;&#039;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **array** | <br />sender channel structure |
| `$type` | **string** | <br />packet type: one of &#039;ping&#039;, &#039;pickup&#039;, &#039;purge&#039;, &#039;refresh&#039;, &#039;keychange&#039;, &#039;force_refresh&#039;, &#039;notify&#039;, &#039;auth_check&#039; |
| `$recipients` | **array** | <br />envelope recipients, array of portable_id&#039;s; empty for public posts |
| `$msg` | **array** | <br />optional message |
| `$encoding` | **string** | <br />optional encoding, default &#039;activitystreams&#039; |
| `$remote_key` | **string** | <br />optional public site key of target hub used to encrypt entire packet<br />NOTE: remote_key and encrypted packets are required for &#039;auth_check&#039; packets, optional for all others |
| `$methods` | **string** | <br />optional comma separated list of encryption methods @ref best_algorithm() |





***

### best_algorithm



```php
public static best_algorithm(string $methods): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$methods` | **string** | <br />Comma separated list of encryption methods |


**Return Value:**

first match from our site method preferences Crypto::methods() array
of a method which is common to both sites; or 'aes256cbc' if no matches are found.




***

### zot



```php
public static zot(string $url, string $data, array $channel = null, array $crypto = null): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** |  |
| `$data` | **string** |  |
| `$channel` | **array** | (required if using zot6 delivery) |
| `$crypto` | **array** | (required if encrypted httpsig, requires hubloc_sitekey and site_crypto elements) |


**Return Value:**

see z_post_url() for returned data format




**See Also:**

* \Zotlabs\Lib\z_post_url() - 

***

### refresh



```php
public static refresh(array $them, array $channel = null, bool $force = false): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$them` | **array** | =&gt; xchan structure of sender |
| `$channel` | **array** | =&gt; local channel structure of target recipient, required for &quot;friending&quot; operations |
| `$force` | **bool** | (optional) default false |


**Return Value:**


*  * \b true if successful
*  * otherwise \b false




***

### gethub



```php
public static gethub(array $arr, bool $multiple = false): array|null
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **array** | an associative array which must contain:<br />* \e string \b id =&gt; id of conversant<br />* \e string \b id_sig =&gt; id signed with conversant&#039;s private key<br />* \e string \b location =&gt; URL of the origination hub of this communication<br />* \e string \b location_sig =&gt; URL signed with conversant&#039;s private key<br />* \e string \b site_id =&gt; URL signed with conversant&#039;s private key |
| `$multiple` | **bool** | (optional) default false |


**Return Value:**


*  * null if site is blacklisted or not found
*  * otherwise an array with an hubloc record




***

### valid_hub



```php
public static valid_hub(string $sender, string $site_id): null|array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sender` | **string** |  |
| `$site_id` | **string** |  |





***

### register_hub



```php
public static register_hub(string $id): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** |  |


**Return Value:**

An associative array with
* \e boolean \b success
* \e string \b message (optional, unused) error string only if success is false




***

### import_xchan



```php
public static import_xchan(array $arr): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **array** | =&gt; json_decoded discovery packet |


**Return Value:**

An associative array with:
* \e boolean \b success boolean true or false
* \e string \b message (optional) error string only if success is false




***

### process_response



```php
public static process_response(string $hub, array $arr, array $outq): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hub` | **string** | - url of site we just contacted |
| `$arr` | **array** | - output of z_post_url() |
| `$outq` | **array** | - The queue structure attached to this request |





***

### fetch



```php
public static fetch(array $arr): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **array** | <br />decrypted and json decoded notify packet from remote site |


**Return Value:**

from zot_import()




**See Also:**

* \Zotlabs\Lib\zot_import() - 

***

### import



```php
public static import(array $arr): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **array** | <br />&#039;pickup&#039; structure returned from remote site |





***

### is_top_level



```php
public static is_top_level(array $env, object $act): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$env` | **array** |  |
| `$act` | **object** |  |





***

### find_parent



```php
public static find_parent(mixed $env, mixed $act): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$env` | **mixed** |  |
| `$act` | **mixed** |  |





***

### find_parent_owner_hashes



```php
public static find_parent_owner_hashes(mixed $env, mixed $act): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$env` | **mixed** |  |
| `$act` | **mixed** |  |





***

### public_recips



```php
public static public_recips(array $msg, object $act): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$msg` | **array** |  |
| `$act` | **object** |  |





***

### process_delivery



```php
public static process_delivery(string $sender, mixed $act, array $arr, array $deliveries, bool $relay, bool $public = false, bool $request = false, bool $force = false, mixed $is_collection_operation = false): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sender` | **string** |  |
| `$act` | **mixed** |  |
| `$arr` | **array** |  |
| `$deliveries` | **array** |  |
| `$relay` | **bool** |  |
| `$public` | **bool** | (optional) default false |
| `$request` | **bool** | (optional) default false |
| `$force` | **bool** | (optional) default false - should only be set for manual fetch |
| `$is_collection_operation` | **mixed** |  |





***

### fetch_conversation



```php
public static fetch_conversation(mixed $channel, mixed $mid, mixed $force = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **mixed** |  |
| `$mid` | **mixed** |  |
| `$force` | **mixed** |  |





***

### remove_community_tag



```php
public static remove_community_tag(string $sender, array $arr, int $uid): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sender` | **string** |  |
| `$arr` | **array** | an associative array<br />* \e int \b verb<br />* \e int \b obj_type<br />* \e int \b mid |
| `$uid` | **int** |  |





***

### update_imported_item



```php
public static update_imported_item(string $sender, array $item, array $orig, int $uid, bool $tag_delivery): void|array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sender` | **string** |  |
| `$item` | **array** |  |
| `$orig` | **array** |  |
| `$uid` | **int** |  |
| `$tag_delivery` | **bool** |  |





**See Also:**

* \Zotlabs\Lib\item_store_update() - 

***

### delete_imported_item



```php
public static delete_imported_item(string $sender, mixed $act, array $item, int $uid, bool $relay): bool|int
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sender` | **string** | <br />*  * \e string \b hash a xchan_hash |
| `$act` | **mixed** |  |
| `$item` | **array** |  |
| `$uid` | **int** |  |
| `$relay` | **bool** |  |


**Return Value:**

post_id




***

### encode_locations



```php
public static encode_locations(array $channel): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **array** | an associative array which must contain<br />* \e string \b channel_hash the hash of the channel |


**Return Value:**

an array with associative arrays




**See Also:**

* \Zotlabs\Lib\self::get_hublocs() - 

***

### import_site



```php
public static import_site(array $arr): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **array** |  |


**Return Value:**

true if updated or inserted




***

### get_rpost_path



```php
public static get_rpost_path(array $observer): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$observer` | **array** | <br />*  * \e string \b xchan_url |





***

### import_author_zot



```php
public static import_author_zot(array $x): bool|string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **array** |  |


**Return Value:**

return false or a hash




***

### zotinfo



```php
public static zotinfo(mixed $arr): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **mixed** |  |





***

### site_info



```php
public static site_info(): array
```



* This method is **static**.








***

### update_hub_connected



```php
public static update_hub_connected(array $hub, string $site_id = &#039;&#039;): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hub` | **array** |  |
| `$site_id` | **string** | (optional, default empty) |


**Return Value:**

hubloc_url




***

### sign



```php
public static sign(string $data, string $key, string $alg = &#039;sha256&#039;): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |
| `$key` | **string** |  |
| `$alg` | **string** | (optional) default &#039;sha256&#039; |





***

### verify



```php
public static verify(mixed $data, mixed $sig, mixed $key): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$sig` | **mixed** |  |
| `$key` | **mixed** |  |





***

### is_zot_request



```php
public static is_zot_request(): bool
```



* This method is **static**.








***

### zot_record_preferred



```php
public static zot_record_preferred(mixed $arr, mixed $check = &#039;hubloc_network&#039;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **mixed** |  |
| `$check` | **mixed** |  |





***

### update_cached_hubloc



```php
public static update_cached_hubloc(mixed $hubloc): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hubloc` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
