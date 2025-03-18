
# InviteReply

This class represents the cs:invite-reply notification element.



* Full name: `\Sabre\CalDAV\Xml\Notification\InviteReply`
* This class implements:
[`\Sabre\CalDAV\Xml\Notification\NotificationInterface`](./NotificationInterface.md)



## Properties


### id

A unique id for the message.

```php
protected string $id
```






***

### dtStamp

Timestamp of the notification.

```php
protected \DateTime $dtStamp
```






***

### inReplyTo

The unique id of the notification this was a reply to.

```php
protected string $inReplyTo
```






***

### href

A url to the recipient of the original (!) notification.

```php
protected string $href
```






***

### type

The type of message, see the SharingPlugin::STATUS_ constants.

```php
protected int $type
```






***

### hostUrl

A url to the shared calendar.

```php
protected string $hostUrl
```






***

### summary

A description of the share request.

```php
protected string $summary
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

Creates the Invite Reply Notification.

```php
public __construct(array $values): mixed
```

This constructor receives an array with the following elements:

* id           - A unique id
* etag         - The etag
* dtStamp      - A DateTime object with a timestamp for the notification.
* inReplyTo    - This should refer to the 'id' of the notification
                 this is a reply to.
* type         - The type of notification, see SharingPlugin::STATUS_*
                 constants for details.
* hostUrl      - A url to the shared calendar.
* summary      - Description of the share, can be the same as the
                 calendar, but may also be modified (optional).






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$values` | **array** |  |





***

### xmlSerialize

The xmlSerialize method is called during xml writing.

```php
public xmlSerialize(\Sabre\Xml\Writer $writer): mixed
```

Use the $writer argument to write its own xml serialization.

An important note: do _not_ create a parent element. Any element
implementing XmlSerializable should only ever write what's considered
its 'inner xml'.

The parent of the current element is responsible for writing a
containing element.

This allows serializers to be re-used for different element names.

If you are opening new elements, you must also close them again.






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
> Automatically generated on 2025-03-18
