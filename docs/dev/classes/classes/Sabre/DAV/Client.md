***

# Client

SabreDAV DAV client.

This client wraps around Curl to provide a convenient API to a WebDAV
server.

NOTE: This class is experimental, it's api will likely change in the future.

* Full name: `\Sabre\DAV\Client`
* Parent class: [`\Sabre\HTTP\Client`](../HTTP/Client.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`AUTH_BASIC`|public| |1|
|`AUTH_DIGEST`|public| |2|
|`AUTH_NTLM`|public| |4|
|`ENCODING_IDENTITY`|public| |1|
|`ENCODING_DEFLATE`|public| |2|
|`ENCODING_GZIP`|public| |4|
|`ENCODING_ALL`|public| |7|

## Properties


### xml

The xml service.

```php
public mixed $xml
```

Uset this service to configure the property and namespace maps.




***

### propertyMap

The elementMap.

```php
public array $propertyMap
```

This property is linked via reference to $this->xml->elementMap.
It's deprecated as of version 3.0.0, and should no longer be used.


* **Warning:** this property is **deprecated**. This means that this property will likely be removed in a future version.



***

### baseUri

Base URI.

```php
protected string $baseUri
```

This URI will be used to resolve relative urls.




***

### encoding

Content-encoding.

```php
protected int $encoding
```






***

## Methods


### __construct

Constructor.

```php
public __construct(array $settings): mixed
```

Settings are provided through the 'settings' argument. The following
settings are supported:

  * baseUri
  * userName (optional)
  * password (optional)
  * proxy (optional)
  * authType (optional)
  * encoding (optional)

 authType must be a bitmap, using self::AUTH_BASIC, self::AUTH_DIGEST
 and self::AUTH_NTLM. If you know which authentication method will be
 used, it's recommended to set it, as it will save a great deal of
 requests to 'discover' this information.

 Encoding is a bitmap with one of the ENCODING constants.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$settings` | **array** |  |





***

### propFind

Does a PROPFIND request with filtered response returning only available properties.

```php
public propFind(mixed $url, array $properties, 1|0 $depth): array
```

The list of requested properties must be specified as an array, in clark
notation.

Depth should be either 0 or 1. A depth of 1 will cause a request to be
made to the server to also return all child resources.

For depth 0, just the array of properties for the resource is returned.

For depth 1, the returned array will contain a list of resource names as keys,
and an array of properties as values.

The array of properties will contain the properties as keys with their values as the value.
Only properties that are actually returned from the server without error will be
returned, anything else is discarded.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$properties` | **array** |  |
| `$depth` | **1&#124;0** |  |





***

### propFindUnfiltered

Does a PROPFIND request with unfiltered response.

```php
public propFindUnfiltered(string $url, array $properties, 1|0 $depth): array
```

The list of requested properties must be specified as an array, in clark
notation.

Depth should be either 0 or 1. A depth of 1 will cause a request to be
made to the server to also return all child resources.

For depth 0, just the multi-level array of status and properties for the resource is returned.

For depth 1, the returned array will contain a list of resources as keys and
a multi-level array containing status and properties as value.

The multi-level array of status and properties is formatted the same as what is
documented for parseMultiStatus.

All properties that are actually returned from the server are returned by this method.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** |  |
| `$properties` | **array** |  |
| `$depth` | **1&#124;0** |  |





***

### doPropFind

Does a PROPFIND request.

```php
private doPropFind(mixed $url, array $properties, 1|0 $depth): array
```

The list of requested properties must be specified as an array, in clark
notation.

Depth should be either 0 or 1. A depth of 1 will cause a request to be
made to the server to also return all child resources.

The returned array will contain a list of resources as keys and
a multi-level array containing status and properties as value.

The multi-level array of status and properties is formatted the same as what is
documented for parseMultiStatus.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$properties` | **array** |  |
| `$depth` | **1&#124;0** |  |





***

### propPatch

Updates a list of properties on the server.

```php
public propPatch(string $url, array $properties): bool
```

The list of properties must have clark-notation properties for the keys,
and the actual (string) value for the value. If the value is null, an
attempt is made to delete the property.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** |  |
| `$properties` | **array** |  |





***

### options

Performs an HTTP options request.

```php
public options(): array
```

This method returns all the features from the 'DAV:' header as an array.
If there was no DAV header, or no contents this method will return an
empty array.










***

### request

Performs an actual HTTP request, and returns the result.

```php
public request(string $method, string $url = &#039;&#039;, string|resource|null $body = null, array $headers = []): array
```

If the specified url is relative, it will be expanded based on the base
url.

The returned array contains 3 keys:
  * body - the response body
  * httpCode - a HTTP code (200, 404, etc)
  * headers - a list of response http headers. The header names have
    been lowercased.

For large uploads, it's highly recommended to specify body as a stream
resource. You can easily do this by simply passing the result of
fopen(..., 'r').

This method will throw an exception if an HTTP error was received. Any
HTTP status code above 399 is considered an error.

Note that it is no longer recommended to use this method, use the send()
method instead.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$method` | **string** |  |
| `$url` | **string** |  |
| `$body` | **string&#124;resource&#124;null** |  |
| `$headers` | **array** |  |




**Throws:**
<p>in case a curl error occurred</p>

- [`clientException`](./clientException.md)



***

### getAbsoluteUrl

Returns the full url based on the given url (which may be relative). All
urls are expanded based on the base url as given by the server.

```php
public getAbsoluteUrl(string $url): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** |  |





***

### parseMultiStatus

Parses a WebDAV multistatus response body.

```php
public parseMultiStatus(string $body): array
```

This method returns an array with the following structure

[
  'url/to/resource' => [
    '200' => [
       '{DAV:}property1' => 'value1',
       '{DAV:}property2' => 'value2',
    ],
    '404' => [
       '{DAV:}property1' => null,
       '{DAV:}property2' => null,
    ],
  ],
  'url/to/resource2' => [
     .. etc ..
  ]
]






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$body` | **string** | xml body |





***


## Inherited methods


### on

Subscribe to an event.

```php
public on(string $eventName, callable $callBack, int $priority = 100): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$eventName` | **string** |  |
| `$callBack` | **callable** |  |
| `$priority` | **int** |  |





***

### once

Subscribe to an event exactly once.

```php
public once(string $eventName, callable $callBack, int $priority = 100): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$eventName` | **string** |  |
| `$callBack` | **callable** |  |
| `$priority` | **int** |  |





***

### emit

Emits an event.

```php
public emit(string $eventName, array $arguments = [], callable $continueCallBack = null): bool
```

This method will return true if 0 or more listeners were successfully
handled. false is returned if one of the events broke the event chain.

If the continueCallBack is specified, this callback will be called every
time before the next event handler is called.

If the continueCallback returns false, event propagation stops. This
allows you to use the eventEmitter as a means for listeners to implement
functionality in your application, and break the event loop as soon as
some condition is fulfilled.

Note that returning false from an event subscriber breaks propagation
and returns false, but if the continue-callback stops propagation, this
is still considered a 'successful' operation and returns true.

Lastly, if there are 5 event handlers for an event. The continueCallback
will be called at most 4 times.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$eventName` | **string** |  |
| `$arguments` | **array** |  |
| `$continueCallBack` | **callable** |  |





***

### listeners

Returns the list of listeners for an event.

```php
public listeners(string $eventName): callable[]
```

The list is returned as an array, and the list of events are sorted by
their priority.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$eventName` | **string** |  |





***

### removeListener

Removes a specific listener from an event.

```php
public removeListener(string $eventName, callable $listener): bool
```

If the listener could not be found, this method will return false. If it
was removed it will return true.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$eventName` | **string** |  |
| `$listener` | **callable** |  |





***

### removeAllListeners

Removes all listeners.

```php
public removeAllListeners(string $eventName = null): mixed
```

If the eventName argument is specified, all listeners for that event are
removed. If it is not specified, every listener for every event is
removed.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$eventName` | **string** |  |





***

### __construct

Initializes the client.

```php
public __construct(): mixed
```












***

### receiveCurlHeader



```php
protected receiveCurlHeader(mixed $curlHandle, mixed $headerLine): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$curlHandle` | **mixed** |  |
| `$headerLine` | **mixed** |  |





***

### send

Sends a request to a HTTP server, and returns a response.

```php
public send(\Sabre\HTTP\RequestInterface $request): \Sabre\HTTP\ResponseInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |





***

### sendAsync

Sends a HTTP request asynchronously.

```php
public sendAsync(\Sabre\HTTP\RequestInterface $request, callable $success = null, callable $error = null): mixed
```

Due to the nature of PHP, you must from time to time poll to see if any
new responses came in.

After calling sendAsync, you must therefore occasionally call the poll()
method, or wait().






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$success` | **callable** |  |
| `$error` | **callable** |  |





***

### poll

This method checks if any http requests have gotten results, and if so,
call the appropriate success or error handlers.

```php
public poll(): bool
```

This method will return true if there are still requests waiting to
return, and false if all the work is done.










***

### wait

Processes every HTTP request in the queue, and waits till they are all
completed.

```php
public wait(): mixed
```












***

### setThrowExceptions

If this is set to true, the Client will automatically throw exceptions
upon HTTP errors.

```php
public setThrowExceptions(bool $throwExceptions): mixed
```

This means that if a response came back with a status code greater than
or equal to 400, we will throw a ClientHttpException.

This only works for the send() method. Throwing exceptions for
sendAsync() is not supported.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$throwExceptions` | **bool** |  |





***

### addCurlSetting

Adds a CURL setting.

```php
public addCurlSetting(int $name, mixed $value): mixed
```

These settings will be included in every HTTP request.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **int** |  |
| `$value` | **mixed** |  |





***

### doRequest

This method is responsible for performing a single request.

```php
protected doRequest(\Sabre\HTTP\RequestInterface $request): \Sabre\HTTP\ResponseInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |





***

### createCurlSettingsArray

Turns a RequestInterface object into an array with settings that can be
fed to curl_setopt.

```php
protected createCurlSettingsArray(\Sabre\HTTP\RequestInterface $request): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |





***

### parseResponse



```php
private parseResponse(string $response, mixed $curlHandle): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$response` | **string** |  |
| `$curlHandle` | **mixed** |  |





***

### parseCurlResponse

Parses the result of a curl call in a format that's a bit more
convenient to work with.

```php
protected parseCurlResponse(array $headerLines, string $body, resource $curlHandle): array
```

The method returns an array with the following elements:
* status - one of the 3 STATUS constants.
* curl_errno - A curl error number. Only set if status is
               STATUS_CURLERROR.
* curl_errmsg - A current error message. Only set if status is
                STATUS_CURLERROR.
* response - Response object. Only set if status is STATUS_SUCCESS, or
             STATUS_HTTPERROR.
* http_code - HTTP status code, as an int. Only set if Only set if
              status is STATUS_SUCCESS, or STATUS_HTTPERROR






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$headerLines` | **array** |  |
| `$body` | **string** |  |
| `$curlHandle` | **resource** |  |





***

### parseCurlResult

Parses the result of a curl call in a format that's a bit more
convenient to work with.

```php
protected parseCurlResult(string $response, resource $curlHandle): array
```

The method returns an array with the following elements:
* status - one of the 3 STATUS constants.
* curl_errno - A curl error number. Only set if status is
               STATUS_CURLERROR.
* curl_errmsg - A current error message. Only set if status is
                STATUS_CURLERROR.
* response - Response object. Only set if status is STATUS_SUCCESS, or
             STATUS_HTTPERROR.
* http_code - HTTP status code, as an int. Only set if Only set if
              status is STATUS_SUCCESS, or STATUS_HTTPERROR




* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$response` | **string** |  |
| `$curlHandle` | **resource** |  |





***

### sendAsyncInternal

Sends an asynchronous HTTP request.

```php
protected sendAsyncInternal(\Sabre\HTTP\RequestInterface $request, callable $success, callable $error, int $retryCount): mixed
```

We keep this in a separate method, so we can call it without triggering
the beforeRequest event and don't do the poll().






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$success` | **callable** |  |
| `$error` | **callable** |  |
| `$retryCount` | **int** |  |





***

### curlExec

Calls curl_exec.

```php
protected curlExec(resource $curlHandle): string
```

This method exists so it can easily be overridden and mocked.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$curlHandle` | **resource** |  |





***

### curlStuff

Returns a bunch of information about a curl request.

```php
protected curlStuff(resource $curlHandle): array
```

This method exists so it can easily be overridden and mocked.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$curlHandle` | **resource** |  |





***


***
> Automatically generated on 2025-03-15
