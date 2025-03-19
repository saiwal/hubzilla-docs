
# ActivityStreams





* Full name: `\Zotlabs\Lib\ActivityStreams`



## Properties


### raw



```php
public $raw
```






***

### data



```php
public $data
```






***

### meta



```php
public $meta
```






***

### valid



```php
public $valid
```






***

### deleted



```php
public $deleted
```






***

### portable_id



```php
public $portable_id
```






***

### id



```php
public $id
```






***

### parent_id



```php
public $parent_id
```






***

### type



```php
public $type
```






***

### actor



```php
public $actor
```






***

### obj



```php
public $obj
```






***

### tgt



```php
public $tgt
```






***

### origin



```php
public $origin
```






***

### owner



```php
public $owner
```






***

### signer



```php
public $signer
```






***

### sig



```php
public $sig
```






***

### sigok



```php
public $sigok
```






***

### recips



```php
public $recips
```






***

### raw_recips



```php
public $raw_recips
```






***

### saved_recips



```php
public $saved_recips
```






***

## Methods


### __construct



```php
public __construct(string $string, mixed $portable_id = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |
| `$portable_id` | **mixed** |  |





***

### is_valid



```php
public is_valid(): bool
```









**Return Value:**

Return true if the JSON string could be decoded.




***

### set_recips



```php
public set_recips(mixed $arr): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **mixed** |  |





***

### objprop



```php
public objprop(string $property, mixed $default = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$property` | **string** |  |
| `$default` | **mixed** | return value if property or object not set<br />or object is a string id which could not be fetched. |





***

### collect_recips



```php
public collect_recips(mixed $base = &#039;&#039;, string $namespace = &#039;&#039;): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$base` | **mixed** |  |
| `$namespace` | **string** | (optional) default empty |





***

### expand



```php
public expand(mixed $arr, mixed $base = &#039;&#039;, mixed $namespace = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **mixed** |  |
| `$base` | **mixed** |  |
| `$namespace` | **mixed** |  |





***

### get_namespace



```php
public get_namespace(array $base, string $namespace): string|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$base` | **array** |  |
| `$namespace` | **string** | if not set return empty string |





***

### get_property_obj



```php
public get_property_obj(string $property, array $base = &#039;&#039;, string $namespace = &#039;&#039;): null|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$property` | **string** |  |
| `$base` | **array** | (optional) |
| `$namespace` | **string** | (optional) default empty |





***

### fetch_property



```php
public fetch_property(string $url, mixed $channel = null): null|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** |  |
| `$channel` | **mixed** |  |





***

### is_an_actor



```php
public static is_an_actor(mixed $s): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |





***

### is_response_activity



```php
public static is_response_activity(mixed $s): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |





***

### get_actor



```php
public get_actor(string $property, array $base = &#039;&#039;, string $namespace = &#039;&#039;): null|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$property` | **string** |  |
| `$base` | **array** |  |
| `$namespace` | **string** | (optional) default empty |





***

### get_compound_property



```php
public get_compound_property(string $property, array $base = &#039;&#039;, string $namespace = &#039;&#039;, bool $first = false): null|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$property` | **string** |  |
| `$base` | **array** |  |
| `$namespace` | **string** | (optional) default empty |
| `$first` | **bool** | (optional) default false, if true and result is a sequential array return only the first element |





***

### is_url



```php
public is_url(string $url): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** |  |





***

### get_primary_type



```php
public get_primary_type(array $base = &#039;&#039;, string $namespace = &#039;&#039;): null|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$base` | **array** |  |
| `$namespace` | **string** | (optional) default empty |





***

### debug



```php
public debug(): mixed
```












***

### is_as_request



```php
public static is_as_request(mixed $channel = null): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **mixed** |  |





***

### get_accept_header_string



```php
public static get_accept_header_string(mixed $channel = null): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **mixed** |  |





***

### checkEddsaSignature



```php
public checkEddsaSignature(): mixed
```












***


***
> Automatically generated on 2025-03-19
