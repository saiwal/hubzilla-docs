
# Activity





* Full name: `\Zotlabs\Lib\Activity`




## Methods


### encode_object



```php
public static encode_object(mixed $x): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **mixed** |  |





***

### fetch_local



```php
public static fetch_local(mixed $url, mixed $portable_id): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$portable_id` | **mixed** |  |





***

### fetch



```php
public static fetch(mixed $url, mixed $channel = null): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$channel` | **mixed** |  |





***

### fetch_person



```php
public static fetch_person(mixed $x): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **mixed** |  |





***

### fetch_profile



```php
public static fetch_profile(mixed $x): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **mixed** |  |





***

### fetch_thing



```php
public static fetch_thing(mixed $x): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **mixed** |  |





***

### fetch_item



```php
public static fetch_item(mixed $x): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **mixed** |  |





***

### fetch_image



```php
public static fetch_image(mixed $x): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **mixed** |  |





***

### fetch_event



```php
public static fetch_event(mixed $x): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **mixed** |  |





***

### paged_collection_init



```php
public static paged_collection_init(mixed $total, mixed $id, mixed $type = &#039;OrderedCollection&#039;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$total` | **mixed** |  |
| `$id` | **mixed** |  |
| `$type` | **mixed** |  |





***

### encode_item_collection



```php
public static encode_item_collection(mixed $items, mixed $id, mixed $type, mixed $total): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$items` | **mixed** |  |
| `$id` | **mixed** |  |
| `$type` | **mixed** |  |
| `$total` | **mixed** |  |





***

### encode_follow_collection



```php
public static encode_follow_collection(mixed $items, mixed $id, mixed $type, mixed $extra = null): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$items` | **mixed** |  |
| `$id` | **mixed** |  |
| `$type` | **mixed** |  |
| `$extra` | **mixed** |  |





***

### encode_simple_collection



```php
public static encode_simple_collection(mixed $items, mixed $id, mixed $type, mixed $total, mixed $extra = null): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$items` | **mixed** |  |
| `$id` | **mixed** |  |
| `$type` | **mixed** |  |
| `$total` | **mixed** |  |
| `$extra` | **mixed** |  |





***

### encode_item



```php
public static encode_item(mixed $i): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$i` | **mixed** |  |





***

### decode_taxonomy



```php
public static decode_taxonomy(mixed $item): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |





***

### encode_taxonomy



```php
public static encode_taxonomy(mixed $item): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |





***

### encode_attachment



```php
public static encode_attachment(mixed $item, mixed $iconfig = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |
| `$iconfig` | **mixed** |  |





***

### decode_iconfig



```php
public static decode_iconfig(mixed $item): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |





***

### decode_attachment



```php
public static decode_attachment(mixed $item): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |





***

### encode_activity



```php
public static encode_activity(mixed $i, mixed $recurse = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$i` | **mixed** |  |
| `$recurse` | **mixed** |  |





***

### map_mentions



```php
public static map_mentions(mixed $i): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$i` | **mixed** |  |





***

### map_acl



```php
public static map_acl(mixed $i): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$i` | **mixed** |  |





***

### lookup_term_url



```php
public static lookup_term_url(mixed $url): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### encode_person



```php
public static encode_person(mixed $p, mixed $extended = true): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$p` | **mixed** |  |
| `$extended` | **mixed** |  |





***

### encode_item_object



```php
public static encode_item_object(mixed $item, mixed $elm = &#039;obj&#039;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |
| `$elm` | **mixed** |  |





***

### activity_mapper



```php
public static activity_mapper(mixed $verb): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$verb` | **mixed** |  |





***

### activity_obj_mapper



```php
public static activity_obj_mapper(mixed $obj): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **mixed** |  |





***

### follow



```php
public static follow(mixed $channel, mixed $act): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **mixed** |  |
| `$act` | **mixed** |  |





***

### unfollow



```php
public static unfollow(mixed $channel, mixed $act): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **mixed** |  |
| `$act` | **mixed** |  |





***

### drop



```php
public static drop(mixed $channel, mixed $observer, mixed $act): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **mixed** |  |
| `$observer` | **mixed** |  |
| `$act` | **mixed** |  |





***

### actor_store



```php
public static actor_store(mixed $person_obj, mixed $force = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$person_obj` | **mixed** |  |
| `$force` | **mixed** |  |





***

### vid_sort



```php
public static vid_sort(mixed $a, mixed $b): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$a` | **mixed** |  |
| `$b` | **mixed** |  |





***

### get_actor_bbmention



```php
public static get_actor_bbmention(mixed $id): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |





***

### update_poll



```php
public static update_poll(mixed $pollItem, mixed $response): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pollItem` | **mixed** |  |
| `$response` | **mixed** |  |





***

### decode_note



```php
public static decode_note(mixed $act): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$act` | **mixed** |  |





***

### store



```php
public static store(mixed $channel, mixed $observer_hash, mixed $act, mixed $item, mixed $fetch_parents = true, mixed $force = false, mixed $is_collection_operation = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **mixed** |  |
| `$observer_hash` | **mixed** |  |
| `$act` | **mixed** |  |
| `$item` | **mixed** |  |
| `$fetch_parents` | **mixed** |  |
| `$force` | **mixed** |  |
| `$is_collection_operation` | **mixed** |  |





***

### fetch_and_store_parents



```php
public static fetch_and_store_parents(array $channel, array $observer_hash, array $item, object $act = null, bool $force = false): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **array** |  |
| `$observer_hash` | **array** |  |
| `$item` | **array** | string&amp;#124;array |
| `$act` | **object** | activitystreams object (optional) default null |
| `$force` | **bool** | disregard permissions and force storage (optional) default false |





***

### bb_attach



```php
public static bb_attach(mixed $item): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |





***

### media_not_in_body



```php
public static media_not_in_body(mixed $s, mixed $body): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |
| `$body` | **mixed** |  |





***

### bb_content



```php
public static bb_content(mixed $content, mixed $field): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$content` | **mixed** |  |
| `$field` | **mixed** |  |





***

### get_content



```php
public static get_content(mixed $act): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$act` | **mixed** |  |





***

### get_textfield



```php
public static get_textfield(mixed $act, mixed $field): null|string|array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$act` | **mixed** |  |
| `$field` | **mixed** |  |





***

### token_from_request



```php
public static token_from_request(): mixed
```



* This method is **static**.








***

### find_best_identity



```php
public static find_best_identity(mixed $xchan): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$xchan` | **mixed** |  |





***

### get_cached_actor



```php
public static get_cached_actor(mixed $id): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |





***

### get_actor



```php
public static get_actor(mixed $actor_id, mixed $force = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$actor_id` | **mixed** |  |
| `$force` | **mixed** |  |





***

### get_unknown_actor



```php
public static get_unknown_actor(mixed $act): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$act` | **mixed** |  |





***

### get_actor_hublocs



```php
public static get_actor_hublocs(mixed $url, mixed $options = &#039;all&#039;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$options` | **mixed** |  |





***

### get_actor_collections



```php
public static get_actor_collections(mixed $url): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### get_actor_protocols



```php
public static get_actor_protocols(mixed $actor): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$actor` | **mixed** |  |





***

### get_quote_bbcode



```php
public static get_quote_bbcode(mixed $url): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### get_attributed_to_actor_url



```php
public static get_attributed_to_actor_url(mixed $act): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$act` | **mixed** |  |





***

### ap_context



```php
public static ap_context(mixed $contextType = null): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$contextType` | **mixed** |  |





***

### ap_schema



```php
public static ap_schema(mixed $contextType = null): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$contextType` | **mixed** |  |





***

### build_packet



```php
public static build_packet(array $obj, array $channel = [], bool $json_encode = true): string|array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **array** |  |
| `$channel` | **array** | (optional) default [] |
| `$json_encode` | **bool** | (optional) default true |





***

### init_background_fetch



```php
public static init_background_fetch(string $observer_hash = &#039;&#039;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$observer_hash` | **string** |  |





***

### addToCollection



```php
public static addToCollection(mixed $channel, mixed $object, mixed $target, mixed $sourceItem = null, mixed $deliver = true): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **mixed** |  |
| `$object` | **mixed** |  |
| `$target` | **mixed** |  |
| `$sourceItem` | **mixed** |  |
| `$deliver` | **mixed** |  |





***

### removeFromCollection



```php
public static removeFromCollection(mixed $channel, mixed $object, mixed $target, mixed $deliver = true): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **mixed** |  |
| `$object` | **mixed** |  |
| `$target` | **mixed** |  |
| `$deliver` | **mixed** |  |





***


***
> Automatically generated on 2025-03-19
