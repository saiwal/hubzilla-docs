
# NotificationInterface

This interface reflects a single notification type.



* Full name: `\Sabre\CalDAV\Xml\Notification\NotificationInterface`
* Parent interfaces: [`\Sabre\Xml\XmlSerializable`](../../../Xml/XmlSerializable.md)


## Methods


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


## Inherited methods


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


***
> Automatically generated on 2025-03-18
