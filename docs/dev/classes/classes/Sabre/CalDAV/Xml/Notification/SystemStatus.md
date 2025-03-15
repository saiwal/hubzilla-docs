***

# SystemStatus

SystemStatus notification.

This notification can be used to indicate to the user that the system is
down.

* Full name: `\Sabre\CalDAV\Xml\Notification\SystemStatus`
* This class implements:
[`\Sabre\CalDAV\Xml\Notification\NotificationInterface`](./NotificationInterface.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`TYPE_LOW`|public| |1|
|`TYPE_MEDIUM`|public| |2|
|`TYPE_HIGH`|public| |3|

## Properties


### id

A unique id.

```php
protected string $id
```






***

### type

The type of alert. This should be one of the TYPE_ constants.

```php
protected int $type
```






***

### description

A human-readable description of the problem.

```php
protected string $description
```






***

### href

A url to a website with more information for the user.

```php
protected string $href
```






***

### etag

Notification Etag.

```php
protected string $etag
```






***

## Methods


### __construct

Creates the notification.

```php
public __construct(string $id, string $etag, int $type = self::TYPE_HIGH, string $description = null, string $href = null): mixed
```

Some kind of unique id should be provided. This is used to generate a
url.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** |  |
| `$etag` | **string** |  |
| `$type` | **int** |  |
| `$description` | **string** |  |
| `$href` | **string** |  |





***

### xmlSerialize

The serialize method is called during xml writing.

```php
public xmlSerialize(\Sabre\Xml\Writer $writer): mixed
```

It should use the $writer argument to encode this object into XML.

Important note: it is not needed to create the parent element. The
parent element is already created, and we only have to worry about
attributes, child elements and text (if any).

Important note 2: If you are writing any new elements, you are also
responsible for closing them.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$writer` | **\Sabre\Xml\Writer** |  |





***

### xmlSerializeFull

This method serializes the entire notification, as it is used in the
response body.

```php
public xmlSerializeFull(\Sabre\Xml\Writer $writer): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$writer` | **\Sabre\Xml\Writer** |  |





***

### getId

Returns a unique id for this notification.

```php
public getId(): string
```

This is just the base url. This should generally be some kind of unique
id.










***

### getETag

Returns the ETag for this notification.

```php
public getETag(): string
```

The ETag must be surrounded by literal double-quotes.










***


***
> Automatically generated on 2025-03-15
