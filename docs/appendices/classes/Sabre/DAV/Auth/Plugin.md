
# Plugin

This plugin provides Authentication for a WebDAV server.

It works by providing a Auth\Backend class. Several examples of these
classes can be found in the Backend directory.

It's possible to provide more than one backend to this plugin. If more than
one backend was provided, each backend will attempt to authenticate. Only if
all backends fail, we throw a 401.

* Full name: `\Sabre\DAV\Auth\Plugin`
* Parent class: [`\Sabre\DAV\ServerPlugin`](../ServerPlugin.md)



## Properties


### autoRequireLogin

By default this plugin will require that the user is authenticated,
and refuse any access if the user is not authenticated.

```php
public $autoRequireLogin
```

If this setting is set to false, we let the user through, whether they
are authenticated or not.

This is useful if you want to allow both authenticated and
unauthenticated access to your server.




***

### backends

authentication backends.

```php
protected $backends
```






***

### currentPrincipal

The currently logged in principal. Will be `null` if nobody is currently
logged in.

```php
protected string|null $currentPrincipal
```






***

### loginFailedReasons

List of reasons why login failed for the last login operation.

```php
protected string[]|null $loginFailedReasons
```






***

## Methods


### __construct

Creates the authentication plugin.

```php
public __construct(\Sabre\DAV\Auth\Backend\BackendInterface $authBackend = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$authBackend` | **\Sabre\DAV\Auth\Backend\BackendInterface** |  |





***

### addBackend

Adds an authentication backend to the plugin.

```php
public addBackend(\Sabre\DAV\Auth\Backend\BackendInterface $authBackend): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$authBackend` | **\Sabre\DAV\Auth\Backend\BackendInterface** |  |





***

### initialize

Initializes the plugin. This function is automatically called by the server.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





***

### getPluginName

Returns a plugin name.

```php
public getPluginName(): string
```

Using this name other plugins will be able to access other plugins
using DAV\Server::getPlugin










***

### getCurrentPrincipal

Returns the currently logged-in principal.

```php
public getCurrentPrincipal(): string|null
```

This will return a string such as:

principals/username
principals/users/username

This method will return null if nobody is logged in.










***

### beforeMethod

This method is called before any HTTP method and forces users to be authenticated.

```php
public beforeMethod(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### check

Checks authentication credentials, and logs the user in if possible.

```php
public check(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): array
```

This method returns an array. The first item in the array is a boolean
indicating if login was successful.

If login was successful, the second item in the array will contain the
current principal url/path of the logged in user.

If login was not successful, the second item in the array will contain a
an array with strings. The strings are a list of reasons why login was
unsuccessful. For every auth backend there will be one reason, so usually
there's just one.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### challenge

This method sends authentication challenges to the user.

```php
public challenge(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): mixed
```

This method will for example cause a HTTP Basic backend to set a
WWW-Authorization header, indicating to the client that it should
authenticate.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### getLoginFailedReasons

Returns a list of reasons why login was unsuccessful.

```php
public getLoginFailedReasons(): string[]|null
```

This method will return the login failed reasons for the last login
operation. One for each auth backend.

This method returns null if the last authentication attempt was
successful, or if there was no authentication attempt yet.










***

### getPluginInfo

Returns a bunch of meta-data about the plugin.

```php
public getPluginInfo(): array
```

Providing this information is optional, and is mainly displayed by the
Browser plugin.

The description key in the returned array may contain html and will not
be sanitized.










***


## Inherited methods


### initialize

This initializes the plugin.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```

This function is called by Sabre\DAV\Server, after
addPlugin is called.

This method should set up the required event subscriptions.


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





***

### getFeatures

This method should return a list of server-features.

```php
public getFeatures(): array
```

This is for example 'versioning' and is added to the DAV: header
in an OPTIONS response.










***

### getHTTPMethods

Use this method to tell the server this plugin defines additional
HTTP methods.

```php
public getHTTPMethods(string $path): array
```

This method is passed a uri. It should only return HTTP methods that are
available for the specified uri.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### getPluginName

Returns a plugin name.

```php
public getPluginName(): string
```

Using this name other plugins will be able to access other plugins
using \Sabre\DAV\Server::getPlugin










***

### getSupportedReportSet

Returns a list of reports this plugin supports.

```php
public getSupportedReportSet(string $uri): array
```

This will be used in the {DAV:}supported-report-set property.
Note that you still need to subscribe to the 'report' event to actually
implement them






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |





***

### getPluginInfo

Returns a bunch of meta-data about the plugin.

```php
public getPluginInfo(): array
```

Providing this information is optional, and is mainly displayed by the
Browser plugin.

The description key in the returned array may contain html and will not
be sanitized.










***


***
> Automatically generated on 2025-03-18
