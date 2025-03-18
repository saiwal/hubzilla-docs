
# AccessList





* Full name: `\Zotlabs\Access\AccessList`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`REQUIRED_KEYS_CONSTRUCTOR`|private| |[&#039;channel_allow_cid&#039;, &#039;channel_allow_gid&#039;, &#039;channel_deny_cid&#039;, &#039;channel_deny_gid&#039;]|
|`REQUIRED_KEYS_SET`|private| |[&#039;allow_cid&#039;, &#039;allow_gid&#039;, &#039;deny_cid&#039;, &#039;deny_gid&#039;]|

## Properties


### allow_cid



```php
private string $allow_cid
```






***

### allow_gid



```php
private string $allow_gid
```






***

### deny_cid



```php
private string $deny_cid
```






***

### deny_gid



```php
private string $deny_gid
```






***

### explicit



```php
private bool $explicit
```






***

## Methods


### __construct



```php
public __construct(array $channel): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **array** | A channel array, where these entries are evaluated:<br />* \e string \b channel_allow_cid =&gt; string of allowed cids<br />* \e string \b channel_allow_gid =&gt; string of allowed gids<br />* \e string \b channel_deny_cid =&gt; string of denied cids<br />* \e string \b channel_deny_gid =&gt; string of denied gids |





***

### validate_input_array



```php
private validate_input_array(array $arr, array $required_keys): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **array** |  |
| `$required_keys` | **array** |  |





***

### get_explicit



```php
public get_explicit(): bool
```












***

### set



```php
public set(array $arr, bool $explicit = true): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **array** | <br />*  * \e string \b allow_cid =&gt; string of allowed cids<br />*  * \e string \b allow_gid =&gt; string of allowed gids<br />*  * \e string \b deny_cid  =&gt; string of denied cids<br />*  * \e string \b deny_gid  =&gt; string of denied gids |
| `$explicit` | **bool** | (optional) default true |





***

### get



```php
public get(): array
```









**Return Value:**

An associative array with:
* \e string \b allow_cid => string of allowed cids
* \e string \b allow_gid => string of allowed gids
* \e string \b deny_cid  => string of denied cids
* \e string \b deny_gid  => string of denied gids




***

### set_from_array



```php
public set_from_array(array $arr, bool $explicit = true): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **array** | An associative array with:<br />* \e array&amp;#124;string \b contact_allow =&gt; array with cids or comma-seperated string<br />* \e array&amp;#124;string \b group_allow   =&gt; array with gids or comma-seperated string<br />* \e array&amp;#124;string \b contact_deny  =&gt; array with cids or comma-seperated string<br />* \e array&amp;#124;string \b group_deny    =&gt; array with gids or comma-seperated string |
| `$explicit` | **bool** | (optional) default true |





***

### is_private



```php
public is_private(): bool
```









**Return Value:**

Return true if any of allow_* deny_* values is set.




***


***
> Automatically generated on 2025-03-18
