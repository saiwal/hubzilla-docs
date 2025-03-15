***

# LightOpenID

This class provides a simple interface for OpenID (1.1 and 2.0) authentication.

Supports Yadis discovery.
The authentication process is stateless/dumb.

Usage:
Sign-on with OpenID is a two step process:
Step one is authentication with the provider:
<code>
$openid = new LightOpenID('my-host.example.org');
$openid->identity = 'ID supplied by user';
header('Location: ' . $openid->authUrl());
</code>
The provider then sends various parameters via GET, one of them is openid_mode.
Step two is verification:
<code>
if ($this->data['openid_mode']) {
    $openid = new LightOpenID('my-host.example.org');
    echo $openid->validate() ? 'Logged in.' : 'Failed';
}
</code>

Change the 'my-host.example.org' to your domain name. Do NOT use $_SERVER['HTTP_HOST']
for that, unless you know what you are doing.

Optionally, you can set $returnUrl and $realm (or $trustRoot, which is an alias).
The default values for those are:
$openid->realm     = (!empty($_SERVER['HTTPS']) ? 'https' : 'http') . '://' . $_SERVER['HTTP_HOST'];
$openid->returnUrl = $openid->realm . $_SERVER['REQUEST_URI'];
If you don't know their meaning, refer to any openid tutorial, or specification. Or just guess.

AX and SREG extensions are supported.
To use them, specify $openid->required and/or $openid->optional before calling $openid->authUrl().
These are arrays, with values being AX schema paths (the 'path' part of the URL).
For example:
  $openid->required = array('namePerson/friendly', 'contact/email');
  $openid->optional = array('namePerson/first');
If the server supports only SREG or OpenID 1.1, these are automaticaly
mapped to SREG names, so that user doesn't have to know anything about the server.

To get the values, use $openid->getAttributes().


The library requires PHP >= 5.1.2 with curl or http/https stream wrappers enabled.

* Full name: `\LightOpenID`



## Properties


### returnUrl



```php
public $returnUrl
```






***

### required



```php
public $required
```






***

### optional



```php
public $optional
```






***

### verify_peer



```php
public $verify_peer
```






***

### capath



```php
public $capath
```






***

### cainfo



```php
public $cainfo
```






***

### data



```php
public $data
```






***

### identity



```php
private $identity
```






***

### claimed_id



```php
private $claimed_id
```






***

### server



```php
protected $server
```






***

### version



```php
protected $version
```






***

### trustRoot



```php
protected $trustRoot
```






***

### aliases



```php
protected $aliases
```






***

### identifier_select



```php
protected $identifier_select
```






***

### ax



```php
protected $ax
```






***

### sreg



```php
protected $sreg
```






***

### setup_url



```php
protected $setup_url
```






***

### ax_to_sreg



```php
protected static $ax_to_sreg
```



* This property is **static**.


***

## Methods


### __construct



```php
public __construct(mixed $host): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$host` | **mixed** |  |





***

### __set



```php
public __set(mixed $name, mixed $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |
| `$value` | **mixed** |  |





***

### __get



```php
public __get(mixed $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |





***

### hostExists

Checks if the server specified in the url exists.

```php
public hostExists(mixed $url): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** | url to check |





***

### request_curl



```php
protected request_curl(mixed $url, mixed $method = &#039;GET&#039;, mixed $params = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$method` | **mixed** |  |
| `$params` | **mixed** |  |





***

### request_streams



```php
protected request_streams(mixed $url, mixed $method = &#039;GET&#039;, mixed $params = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$method` | **mixed** |  |
| `$params` | **mixed** |  |





***

### request



```php
protected request(mixed $url, mixed $method = &#039;GET&#039;, mixed $params = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$method` | **mixed** |  |
| `$params` | **mixed** |  |





***

### build_url



```php
protected build_url(mixed $url, mixed $parts): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$parts` | **mixed** |  |





***

### htmlTag

Helper function used to scan for <meta>/<link> tags and extract information
from them

```php
protected htmlTag(mixed $content, mixed $tag, mixed $attrName, mixed $attrValue, mixed $valueName): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$content` | **mixed** |  |
| `$tag` | **mixed** |  |
| `$attrName` | **mixed** |  |
| `$attrValue` | **mixed** |  |
| `$valueName` | **mixed** |  |





***

### discover

Performs Yadis and HTML discovery. Normally not used.

```php
public discover(mixed $url): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** | Identity URL. |


**Return Value:**

OP Endpoint (i.e. OpenID provider address).



**Throws:**

- [`ErrorException`](./ErrorException.md)



***

### sregParams



```php
protected sregParams(): mixed
```












***

### axParams



```php
protected axParams(): mixed
```












***

### authUrl_v1



```php
protected authUrl_v1(mixed $immediate): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$immediate` | **mixed** |  |





***

### authUrl_v2



```php
protected authUrl_v2(mixed $immediate): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$immediate` | **mixed** |  |





***

### authUrl

Returns authentication url. Usually, you want to redirect your user to it.

```php
public authUrl(mixed $immediate = false): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$immediate` | **mixed** |  |


**Return Value:**

The authentication url.



**Throws:**

- [`ErrorException`](./ErrorException.md)



***

### validate

Performs OpenID verification with the OP.

```php
public validate(): bool
```









**Return Value:**

Whether the verification was successful.



**Throws:**

- [`ErrorException`](./ErrorException.md)



***

### getAxAttributes



```php
protected getAxAttributes(): mixed
```












***

### getSregAttributes



```php
protected getSregAttributes(): mixed
```












***

### getAttributes

Gets AX/SREG attributes provided by OP. should be used only after successful validaton.

```php
public getAttributes(): mixed
```

Note that it does not guarantee that any of the required/optional parameters will be present,
or that there will be no other attributes besides those specified.
In other words. OP may provide whatever information it wants to.
    * SREG names will be mapped to AX names.
    * @return Array Array of attributes with keys being the AX schema names, e.g. 'contact/email'










**See Also:**

* http://www.axschema.org/types/ - 

***


***
> Automatically generated on 2025-03-15
