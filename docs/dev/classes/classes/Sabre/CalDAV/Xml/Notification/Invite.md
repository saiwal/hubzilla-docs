
# Invite

This class represents the cs:invite-notification notification element.

This element is defined here:
http://svn.calendarserver.org/repository/calendarserver/CalendarServer/trunk/doc/Extensions/caldav-sharing.txt

* Full name: `\Sabre\CalDAV\Xml\Notification\Invite`
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

### href

A url to the recipient of the notification. This can be an email
address (mailto:), or a principal url.

```php
protected string $href
```






***

### type

The type of message, see the SharingPlugin::STATUS_* constants.

```php
protected int $type
```






***

### readOnly

True if access to a calendar is read-only.

```php
protected bool $readOnly
```






***

### hostUrl

A url to the shared calendar.

```php
protected string $hostUrl
```






***

### organizer

Url to the sharer of the calendar.

```php
protected string $organizer
```






***

### commonName

The name of the sharer.

```php
protected string $commonName
```






***

### firstName

The name of the sharer.

```php
protected string $firstName
```






***

### lastName

The name of the sharer.

```php
protected string $lastName
```






***

### summary

A description of the share request.

```php
protected string $summary
```






***

### etag

The Etag for the notification.

```php
protected string $etag
```






***

### supportedComponents

The list of supported components.

```php
protected \Sabre\CalDAV\Xml\Property\SupportedCalendarComponentSet $supportedComponents
```






***

## Methods


### __construct

Creates the Invite notification.

```php
public __construct(array $values): mixed
```

This constructor receives an array with the following elements:

* id           - A unique id
* etag         - The etag
* dtStamp      - A DateTime object with a timestamp for the notification.
* type         - The type of notification, see SharingPlugin::STATUS_*
                 constants for details.
* readOnly     - This must be set to true, if this is an invite for
                 read-only access to a calendar.
* hostUrl      - A url to the shared calendar.
* organizer    - Url to the sharer principal.
* commonName   - The real name of the sharer (optional).
* firstName    - The first name of the sharer (optional).
* lastName     - The last name of the sharer (optional).
* summary      - Description of the share, can be the same as the
                 calendar, but may also be modified (optional).
* supportedComponents - An instance of
                 Sabre\CalDAV\Property\SupportedCalendarComponentSet.
                 This allows the client to determine which components
                 will be supported in the shared calendar. This is
                 also optional.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$values` | **array** | All the options |





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
> Automatically generated on 2025-03-15
