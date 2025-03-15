***

# Client

A rudimentary HTTP client.

This object wraps PHP's curl extension and provides an easy way to send it a
Request object, and return a Response object.

This is by no means intended as the next best HTTP client, but it does the
job and provides a simple integration with the rest of sabre/http.

This client emits the following events:
  beforeRequest(RequestInterface $request)
  afterRequest(RequestInterface $request, ResponseInterface $response)
  error(RequestInterface $request, ResponseInterface $response, bool &$retry, int $retryCount)
  exception(RequestInterface $request, ClientException $e, bool &$retry, int $retryCount)

The beforeRequest event allows you to do some last minute changes to the
request before it's done, such as adding authentication headers.

The afterRequest event will be emitted after the request is completed
successfully.

If a HTTP error is returned (status code higher than 399) the error event is
triggered. It's possible using this event to retry the request, by setting
retry to true.

The amount of times a request has retried is passed as $retryCount, which
can be used to avoid retrying indefinitely. The first time the event is
called, this will be 0.

It's also possible to intercept specific http errors, by subscribing to for
example 'error:401'.

* Full name: `\Sabre\HTTP\Client`
* Parent class: [`\Sabre\Event\EventEmitter`](../Event/EventEmitter.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`STATUS_SUCCESS`|public| |0|
|`STATUS_CURLERROR`|public| |1|
|`STATUS_HTTPERROR`|public| |2|

## Properties


### curlSettings

List of curl settings.

```php
protected array $curlSettings
```






***

### throwExceptions

Whether exceptions should be thrown when a HTTP error is returned.

```php
protected bool $throwExceptions
```






***

### maxRedirects

The maximum number of times we'll follow a redirect.

```php
protected int $maxRedirects
```






***

### headerLinesMap



```php
protected $headerLinesMap
```






***

### curlHandle

Cached curl handle.

```php
private resource $curlHandle
```

By keeping this resource around for the lifetime of this object, things
like persistent connections are possible.




***

### curlMultiHandle

Handler for curl_multi requests.

```php
private resource $curlMultiHandle
```

The first time sendAsync is used, this will be created.




***

### curlMultiMap

Has a list of curl handles, as well as their associated success and
error callbacks.

```php
private array $curlMultiMap
```






***

## Methods


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


***
> Automatically generated on 2025-03-15
