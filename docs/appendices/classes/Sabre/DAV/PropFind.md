
# PropFind

This class holds all the information about a PROPFIND request.

It contains the type of PROPFIND request, which properties were requested
and also the returned items.

* Full name: `\Sabre\DAV\PropFind`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`NORMAL`|public| |0|
|`ALLPROPS`|public| |1|
|`PROPNAME`|public| |2|

## Properties


### path

The path that we're fetching properties for.

```php
protected string $path
```






***

### depth

The Depth of the request.

```php
protected int $depth
```

0 means only the current item. 1 means the current item + its children.
It can also be DEPTH_INFINITY if this is enabled in the server.




***

### requestType

The type of request. See the TYPE constants.

```php
protected $requestType
```






***

### properties

A list of requested properties.

```php
protected array $properties
```






***

### result

The result of the operation.

```php
protected array $result
```

The keys in this array are property names.
The values are an array with two elements: the http status code and then
optionally a value.

Example:

[
   "{DAV:}owner" : [404],
   "{DAV:}displayname" : [200, "Admin"]
]




***

### itemsLeft

This is used as an internal counter for the number of properties that do
not yet have a value.

```php
protected int $itemsLeft
```






***

## Methods


### __construct

Creates the PROPFIND object.

```php
public __construct(string $path, array $properties, int $depth, int $requestType = self::NORMAL): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$properties` | **array** |  |
| `$depth` | **int** |  |
| `$requestType` | **int** |  |





***

### handle

Handles a specific property.

```php
public handle(string $propertyName, mixed $valueOrCallBack): mixed
```

This method checks whether the specified property was requested in this
PROPFIND request, and if so, it will call the callback and use the
return value for it's value.

Example:

$propFind->handle('{DAV:}displayname', function() {
     return 'hello';
});

Note that handle will only work the first time. If null is returned, the
value is ignored.

It's also possible to not pass a callback, but immediately pass a value






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propertyName` | **string** |  |
| `$valueOrCallBack` | **mixed** |  |





***

### set

Sets the value of the property.

```php
public set(string $propertyName, mixed $value, int $status = null): mixed
```

If status is not supplied, the status will default to 200 for non-null
properties, and 404 for null properties.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propertyName` | **string** |  |
| `$value` | **mixed** |  |
| `$status` | **int** |  |





***

### get

Returns the current value for a property.

```php
public get(string $propertyName): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propertyName` | **string** |  |





***

### getStatus

Returns the current status code for a property name.

```php
public getStatus(string $propertyName): int|null
```

If the property does not appear in the list of requested properties,
null will be returned.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propertyName` | **string** |  |





***

### setPath

Updates the path for this PROPFIND.

```php
public setPath(string $path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### getPath

Returns the path this PROPFIND request is for.

```php
public getPath(): string
```












***

### getDepth

Returns the depth of this propfind request.

```php
public getDepth(): int
```












***

### setDepth

Updates the depth of this propfind request.

```php
public setDepth(int $depth): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$depth` | **int** |  |





***

### get404Properties

Returns all propertynames that have a 404 status, and thus don't have a
value yet.

```php
public get404Properties(): array
```












***

### getRequestedProperties

Returns the full list of requested properties.

```php
public getRequestedProperties(): array
```

This returns just their names, not a status or value.










***

### isAllProps

Returns true if this was an '{DAV:}allprops' request.

```php
public isAllProps(): bool
```












***

### getResultForMultiStatus

Returns a result array that's often used in multistatus responses.

```php
public getResultForMultiStatus(): array
```

The array uses status codes as keys, and property names and value pairs
as the value of the top array.. such as :

[
 200 => [ '{DAV:}displayname' => 'foo' ],
]










***


***
> Automatically generated on 2025-03-18
