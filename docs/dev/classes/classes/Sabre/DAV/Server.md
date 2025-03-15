
# Server

Main DAV server class.



* Full name: `\Sabre\DAV\Server`
* This class implements:
[`\Psr\Log\LoggerAwareInterface`](../../Psr/Log/LoggerAwareInterface.md), [`\Sabre\Event\EmitterInterface`](../Event/EmitterInterface.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`DEPTH_INFINITY`|public| |-1|
|`NS_SABREDAV`|public| |&#039;http://sabredav.org/ns&#039;|

## Properties


### tree

The tree object.

```php
public \Sabre\DAV\Tree $tree
```






***

### baseUri

The base uri.

```php
protected string $baseUri
```






***

### httpResponse

httpResponse.

```php
public \Sabre\HTTP\Response $httpResponse
```






***

### httpRequest

httpRequest.

```php
public \Sabre\HTTP\Request $httpRequest
```






***

### sapi

PHP HTTP Sapi.

```php
public \Sabre\HTTP\Sapi $sapi
```






***

### plugins

The list of plugins.

```php
protected array $plugins
```






***

### transactionType

This property will be filled with a unique string that describes the
transaction. This is useful for performance measuring and logging
purposes.

```php
public string $transactionType
```

By default it will just fill it with a lowercased HTTP method name, but
plugins override this. For example, the WebDAV-Sync sync-collection
report will set this to 'report-sync-collection'.




***

### protectedProperties

This is a list of properties that are always server-controlled, and
must not get modified with PROPPATCH.

```php
public string[] $protectedProperties
```

Plugins may add to this list.




***

### debugExceptions

This is a flag that allow or not showing file, line and code
of the exception in the returned XML.

```php
public bool $debugExceptions
```






***

### resourceTypeMapping

This property allows you to automatically add the 'resourcetype' value
based on a node's classname or interface.

```php
public array $resourceTypeMapping
```

The preset ensures that {DAV:}collection is automatically added for nodes
implementing Sabre\DAV\ICollection.




***

### enablePropfindDepthInfinity

This property allows the usage of Depth: infinity on PROPFIND requests.

```php
public bool $enablePropfindDepthInfinity
```

By default Depth: infinity is treated as Depth: 1. Allowing Depth:
infinity is potentially risky, as it allows a single client to do a full
index of the webdav server, which is an easy DoS attack vector.

Only turn this on if you know what you're doing.




***

### xml

Reference to the XML utility object.

```php
public \Sabre\DAV\Xml\Service $xml
```






***

### exposeVersion

If this setting is turned off, SabreDAV's version number will be hidden
from various places.

```php
public static bool $exposeVersion
```

Some people feel this is a good security measure.

* This property is **static**.


***

### streamMultiStatus

If this setting is turned on, any multi status response on any PROPFIND will be streamed to the output buffer.

```php
public static bool $streamMultiStatus
```

This will be beneficial for large result sets which will no longer consume a large amount of memory as well as
send back data to the client earlier.

* This property is **static**.


***

## Methods


### __construct

Sets up the server.

```php
public __construct(\Sabre\DAV\Tree|\Sabre\DAV\INode|array|null $treeOrNode = null, \Sabre\HTTP\Sapi $sapi = null): mixed
```

If a Sabre\DAV\Tree object is passed as an argument, it will
use it as the directory tree. If a Sabre\DAV\INode is passed, it
will create a Sabre\DAV\Tree and use the node as the root.

If nothing is passed, a Sabre\DAV\SimpleCollection is created in
a Sabre\DAV\Tree.

If an array is passed, we automatically create a root node, and use
the nodes in the array as top-level children.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$treeOrNode` | **\Sabre\DAV\Tree&#124;\Sabre\DAV\INode&#124;array&#124;null** | The tree object |
| `$sapi` | **\Sabre\HTTP\Sapi** |  |




**Throws:**

- [`Exception`](./Exception.md)



***

### start

Starts the DAV Server.

```php
public start(): mixed
```












***

### exec

Alias of start().

```php
public exec(): mixed
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### setBaseUri

Sets the base server uri.

```php
public setBaseUri(string $uri): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |





***

### getBaseUri

Returns the base responding uri.

```php
public getBaseUri(): string
```












***

### guessBaseUri

This method attempts to detect the base uri.

```php
public guessBaseUri(): string
```

Only the PATH_INFO variable is considered.

If this variable is not set, the root (/) is assumed.










***

### addPlugin

Adds a plugin to the server.

```php
public addPlugin(\Sabre\DAV\ServerPlugin $plugin): mixed
```

For more information, console the documentation of Sabre\DAV\ServerPlugin






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$plugin` | **\Sabre\DAV\ServerPlugin** |  |





***

### getPlugin

Returns an initialized plugin by it's name.

```php
public getPlugin(string $name): \Sabre\DAV\ServerPlugin
```

This function returns null if the plugin was not found.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getPlugins

Returns all plugins.

```php
public getPlugins(): array
```












***

### getLogger

Returns the PSR-3 logger object.

```php
public getLogger(): \Psr\Log\LoggerInterface
```












***

### invokeMethod

Handles a http request, and execute a method based on its name.

```php
public invokeMethod(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response, bool $sendResponse = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |
| `$sendResponse` | **bool** | whether to send the HTTP response to the DAV client |





***

### getAllowedMethods

Returns an array with all the supported HTTP methods for a specific uri.

```php
public getAllowedMethods(string $path): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### getRequestUri

Gets the uri for the request, keeping the base uri into consideration.

```php
public getRequestUri(): string
```












***

### calculateUri

Turns a URI such as the REQUEST_URI into a local path.

```php
public calculateUri(string $uri): string
```

This method:
* strips off the base path
* normalizes the path
* uri-decodes the path






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |




**Throws:**
<p>A permission denied exception is thrown whenever there was an attempt to supply a uri outside of the base uri</p>

- [`Forbidden`](./Exception/Forbidden.md)



***

### getHTTPDepth

Returns the HTTP depth header.

```php
public getHTTPDepth(mixed $default = self::DEPTH_INFINITY): int
```

This method returns the contents of the HTTP depth request header. If the depth header was 'infinity' it will return the Sabre\DAV\Server::DEPTH_INFINITY object
It is possible to supply a default depth value, which is used when the depth header has invalid content, or is completely non-existent






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$default` | **mixed** |  |





***

### getHTTPRange

Returns the HTTP range header.

```php
public getHTTPRange(): int[]|null
```

This method returns null if there is no well-formed HTTP range request
header or array($start, $end).

The first number is the offset of the first byte in the range.
The second number is the offset of the last byte in the range.

If the second offset is null, it should be treated as the offset of the last byte of the entity
If the first offset is null, the second offset should be used to retrieve the last x bytes of the entity










***

### getHTTPPrefer

Returns the HTTP Prefer header information.

```php
public getHTTPPrefer(): array
```

The prefer header is defined in:
http://tools.ietf.org/html/draft-snell-http-prefer-14

This method will return an array with options.

Currently, the following options may be returned:
 [
     'return-asynch'         => true,
     'return-minimal'        => true,
     'return-representation' => true,
     'wait'                  => 30,
     'strict'                => true,
     'lenient'               => true,
 ]

This method also supports the Brief header, and will also return
'return-minimal' if the brief header was set to 't'.

For the boolean options, false will be returned if the headers are not
specified. For the integer options it will be 'null'.










***

### getCopyAndMoveInfo

Returns information about Copy and Move requests.

```php
public getCopyAndMoveInfo(\Sabre\HTTP\RequestInterface $request): array
```

This function is created to help getting information about the source and the destination for the
WebDAV MOVE and COPY HTTP request. It also validates a lot of information and throws proper exceptions

The returned value is an array with the following keys:
  * destination - Destination path
  * destinationExists - Whether or not the destination is an existing url (and should therefore be overwritten)






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |




**Throws:**
<p>upon missing or broken request headers</p>

- [`BadRequest`](./Exception/BadRequest.md)
<p>when trying to copy into a
non-collection</p>

- [`UnsupportedMediaType`](./Exception/UnsupportedMediaType.md)
<p>if overwrite is set to false, but
the destination exists</p>

- [`PreconditionFailed`](./Exception/PreconditionFailed.md)
<p>when source and destination paths are
identical</p>

- [`Forbidden`](./Exception/Forbidden.md)
<p>when trying to copy a node into its own
subtree</p>

- [`Conflict`](./Exception/Conflict.md)



***

### getProperties

Returns a list of properties for a path.

```php
public getProperties(string $path, array $propertyNames): array
```

This is a simplified version getPropertiesForPath. If you aren't
interested in status codes, but you just want to have a flat list of
properties, use this method.

Please note though that any problems related to retrieving properties,
such as permission issues will just result in an empty array being
returned.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$propertyNames` | **array** |  |





***

### getPropertiesForChildren

A kid-friendly way to fetch properties for a node's children.

```php
public getPropertiesForChildren(string $path, array $propertyNames): array
```

The returned array will be indexed by the path of the of child node.
Only properties that are actually found will be returned.

The parent node will not be returned.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$propertyNames` | **array** |  |





***

### getHTTPHeaders

Returns a list of HTTP headers for a particular resource.

```php
public getHTTPHeaders(string $path): array
```

The generated http headers are based on properties provided by the
resource. The method basically provides a simple mapping between
DAV property and HTTP header.

The headers are intended to be used for HEAD and GET requests.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### generatePathNodes

Small helper to support PROPFIND with DEPTH_INFINITY.

```php
private generatePathNodes(\Sabre\DAV\PropFind $propFind, array $yieldFirst = null): \Traversable
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propFind` | **\Sabre\DAV\PropFind** |  |
| `$yieldFirst` | **array** |  |





***

### getPropertiesForPath

Returns a list of properties for a given path.

```php
public getPropertiesForPath(string $path, array $propertyNames = [], int $depth): array
```

The path that should be supplied should have the baseUrl stripped out
The list of properties should be supplied in Clark notation. If the list is empty
'allprops' is assumed.

If a depth of 1 is requested child elements will also be returned.




* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$propertyNames` | **array** |  |
| `$depth` | **int** |  |





**See Also:**

* \Sabre\DAV\getPropertiesIteratorForPath() - 

***

### getPropertiesIteratorForPath

Returns a list of properties for a given path.

```php
public getPropertiesIteratorForPath(string $path, array $propertyNames = [], int $depth): \Iterator
```

The path that should be supplied should have the baseUrl stripped out
The list of properties should be supplied in Clark notation. If the list is empty
'allprops' is assumed.

If a depth of 1 is requested child elements will also be returned.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$propertyNames` | **array** |  |
| `$depth` | **int** |  |





***

### getPropertiesForMultiplePaths

Returns a list of properties for a list of paths.

```php
public getPropertiesForMultiplePaths(array $paths, array $propertyNames = []): array
```

The path that should be supplied should have the baseUrl stripped out
The list of properties should be supplied in Clark notation. If the list is empty
'allprops' is assumed.

The result is returned as an array, with paths for it's keys.
The result may be returned out of order.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$paths` | **array** |  |
| `$propertyNames` | **array** |  |





***

### getPropertiesByNode

Determines all properties for a node.

```php
public getPropertiesByNode(\Sabre\DAV\PropFind $propFind, \Sabre\DAV\INode $node): bool
```

This method tries to grab all properties for a node. This method is used
internally getPropertiesForPath and a few others.

It could be useful to call this, if you already have an instance of your
target node and simply want to run through the system to get a correct
list of properties.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propFind` | **\Sabre\DAV\PropFind** |  |
| `$node` | **\Sabre\DAV\INode** |  |





***

### createFile

This method is invoked by sub-systems creating a new file.

```php
public createFile(string $uri, resource $data, string& $etag = null): bool
```

Currently this is done by HTTP PUT and HTTP LOCK (in the Locks_Plugin).
It was important to get this done through a centralized function,
allowing plugins to intercept this using the beforeCreateFile event.

This method will return true if the file was actually created






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |
| `$data` | **resource** |  |
| `$etag` | **string** |  |





***

### updateFile

This method is invoked by sub-systems updating a file.

```php
public updateFile(string $uri, resource $data, string& $etag = null): bool
```

This method will return true if the file was actually updated






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |
| `$data` | **resource** |  |
| `$etag` | **string** |  |





***

### createDirectory

This method is invoked by sub-systems creating a new directory.

```php
public createDirectory(string $uri): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |





***

### createCollection

Use this method to create a new collection.

```php
public createCollection(string $uri, \Sabre\DAV\MkCol $mkCol): array|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** | The new uri |
| `$mkCol` | **\Sabre\DAV\MkCol** |  |





***

### updateProperties

This method updates a resource's properties.

```php
public updateProperties(string $path, array $properties): array
```

The properties array must be a list of properties. Array-keys are
property names in clarknotation, array-values are it's values.
If a property must be deleted, the value should be null.

Note that this request should either completely succeed, or
completely fail.

The response is an array with properties for keys, and http status codes
as their values.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$properties` | **array** |  |





***

### checkPreconditions

This method checks the main HTTP preconditions.

```php
public checkPreconditions(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```

Currently these are:
  * If-Match
  * If-None-Match
  * If-Modified-Since
  * If-Unmodified-Since

The method will return true if all preconditions are met
The method will return false, or throw an exception if preconditions
failed. If false is returned the operation should be aborted, and
the appropriate HTTP response headers are already set.

Normally this method will throw 412 Precondition Failed for failures
related to If-None-Match, If-Match and If-Unmodified Since. It will
set the status to 304 Not Modified for If-Modified_since.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### getIfConditions

This method is created to extract information from the WebDAV HTTP 'If:' header.

```php
public getIfConditions(\Sabre\HTTP\RequestInterface $request): array
```

The If header can be quite complex, and has a bunch of features. We're using a regex to extract all relevant information
The function will return an array, containing structs with the following keys

  * uri   - the uri the condition applies to.
  * tokens - The lock token. another 2 dimensional array containing 3 elements

Example 1:

If: (<opaquelocktoken:181d4fae-7d8c-11d0-a765-00a0c91e6bf2>)

Would result in:

[
   [
      'uri' => '/request/uri',
      'tokens' => [
         [
             [
                 'negate' => false,
                 'token'  => 'opaquelocktoken:181d4fae-7d8c-11d0-a765-00a0c91e6bf2',
                 'etag'   => ""
             ]
         ]
      ],
   ]
]

Example 2:

If: </path/> (Not <opaquelocktoken:181d4fae-7d8c-11d0-a765-00a0c91e6bf2> ["Im An ETag"]) (["Another ETag"]) </path2/> (Not ["Path2 ETag"])

Would result in:

[
   [
      'uri' => 'path',
      'tokens' => [
         [
             [
                 'negate' => true,
                 'token'  => 'opaquelocktoken:181d4fae-7d8c-11d0-a765-00a0c91e6bf2',
                 'etag'   => '"Im An ETag"'
             ],
             [
                 'negate' => false,
                 'token'  => '',
                 'etag'   => '"Another ETag"'
             ]
         ]
      ],
   ],
   [
      'uri' => 'path2',
      'tokens' => [
         [
             [
                 'negate' => true,
                 'token'  => '',
                 'etag'   => '"Path2 ETag"'
             ]
         ]
      ],
   ],
]






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |





***

### getResourceTypeForNode

Returns an array with resourcetypes for a node.

```php
public getResourceTypeForNode(\Sabre\DAV\INode $node): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\Sabre\DAV\INode** |  |





***

### generateMultiStatus

Returns a callback generating a WebDAV propfind response body based on a list of nodes.

```php
public generateMultiStatus(array|\Traversable $fileProperties, bool $strip404s = false): callable|string
```

If 'strip404s' is set to true, all 404 responses will be removed.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fileProperties` | **array&#124;\Traversable** | The list with nodes |
| `$strip404s` | **bool** |  |





***

### writeMultiStatus



```php
private writeMultiStatus(\Sabre\Xml\Writer $w, mixed $fileProperties, bool $strip404s): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$w` | **\Sabre\Xml\Writer** |  |
| `$fileProperties` | **mixed** |  |
| `$strip404s` | **bool** |  |





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

### setLogger

Sets a logger.

```php
public setLogger(\Psr\Log\LoggerInterface $logger): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$logger` | **\Psr\Log\LoggerInterface** |  |





***


***
> Automatically generated on 2025-03-15
