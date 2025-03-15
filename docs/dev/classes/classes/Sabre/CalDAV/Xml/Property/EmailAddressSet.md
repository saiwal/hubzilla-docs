***

# EmailAddressSet

email-address-set property.

This property represents the email-address-set property in the
http://calendarserver.org/ns/ namespace.

It's a list of email addresses associated with a user.

* Full name: `\Sabre\CalDAV\Xml\Property\EmailAddressSet`
* This class implements:
[`\Sabre\Xml\XmlSerializable`](../../../Xml/XmlSerializable.md)



## Properties


### emails

emails.

```php
private array $emails
```






***

## Methods


### __construct

__construct.

```php
public __construct(array $emails): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$emails` | **array** |  |





***

### getValue

Returns the email addresses.

```php
public getValue(): array
```












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


***
> Automatically generated on 2025-03-15
