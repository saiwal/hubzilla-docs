
# BasicAuth





* Full name: `\Zotlabs\Storage\BasicAuth`
* Parent class: [`AbstractBasic`](../../Sabre/DAV/Auth/Backend/AbstractBasic.md)

**See Also:**

* http://github.com/friendica/red - 



## Properties


### channel_name



```php
protected string|null $channel_name
```






***

### channel_id



```php
public int $channel_id
```






***

### channel_account_id



```php
public int $channel_account_id
```






***

### channel_hash



```php
public string $channel_hash
```






***

### observer



```php
public string $observer
```






***

### browser



```php
public $browser
```





**See Also:**

* \Zotlabs\Storage\Browser::set_writeable() - 

***

### owner_id



```php
public int $owner_id
```






***

### owner_nick

channel_name of the current visited path. Set in Directory::getDir().

```php
public string $owner_nick
```

Used for creating the path in cloud/




***

### timezone

Timezone from the visiting channel's channel_timezone.

```php
protected string $timezone
```

Used in @ref Browser




***

### module_disabled



```php
public $module_disabled
```






***

## Methods


### validateUserPass



```php
protected validateUserPass(string $username, string $password): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |
| `$password` | **string** |  |





**See Also:**

*  - \\Sabre\\DAV\\Auth\\Backend\\AbstractBasic::validateUserPass

***

### setAuthenticated



```php
protected setAuthenticated(mixed $channel): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **mixed** |  |





***

### check

When this method is called, the backend must check if authentication was
successful.

```php
public check(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): array
```

The returned value must be one of the following

[true, "principals/username"]
[false, "reason for failure"]

If authentication was successful, it's expected that the authentication
backend returns a so-called principal url.

Examples of a principal url:

principals/admin
principals/user1
principals/users/joe
principals/uid/123457

If you don't use WebDAV ACL (RFC3744) we recommend that you simply
return a string such as:

principals/users/[username]






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### check_module_access



```php
protected check_module_access(mixed $channel_id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel_id` | **mixed** |  |





***

### setCurrentUser

Sets the channel_name from the currently logged-in channel.

```php
public setCurrentUser(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | <br />The channel&#039;s name |





***

### getCurrentUser

Returns information about the currently logged-in channel.

```php
public getCurrentUser(): string|null
```

If nobody is currently logged in, this method should return null.










**See Also:**

*  - \\Sabre\\DAV\\Auth\\Backend\\AbstractBasic::getCurrentUser

***

### setTimezone



```php
public setTimezone(string $timezone): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$timezone` | **string** | <br />The channel&#039;s timezone. |





***

### getTimezone



```php
public getTimezone(): string
```









**Return Value:**


Return the channel's timezone.




***

### setBrowserPlugin



```php
public setBrowserPlugin(\Sabre\DAV\Browser\Plugin $browser): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$browser` | **\Sabre\DAV\Browser\Plugin** |  |





**See Also:**

* \Zotlabs\Storage\RedBrowser::set_writeable() - 

***

### log



```php
public log(): void
```












***


***
> Automatically generated on 2025-03-15
