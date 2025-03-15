***

# Invite

This class represents the {DAV:}invite property.

This property is defined here:
https://tools.ietf.org/html/draft-pot-webdav-resource-sharing-03#section-4.4.2

This property is used by clients to determine who currently has access to
a shared resource, what their access level is and what their invite status
is.

* Full name: `\Sabre\DAV\Xml\Property\Invite`
* This class implements:
[`\Sabre\Xml\XmlSerializable`](../../../Xml/XmlSerializable.md)



## Properties


### sharees

A list of sharees.

```php
public \Sabre\DAV\Xml\Element\Sharee[] $sharees
```






***

## Methods


### __construct

Creates the property.

```php
public __construct(\Sabre\DAV\Xml\Element\Sharee[] $sharees): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sharees` | **\Sabre\DAV\Xml\Element\Sharee[]** |  |





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
