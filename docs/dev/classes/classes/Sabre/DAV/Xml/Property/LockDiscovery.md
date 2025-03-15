***

# LockDiscovery

Represents {DAV:}lockdiscovery property.

This property is defined here:
http://tools.ietf.org/html/rfc4918#section-15.8

This property contains all the open locks on a given resource

* Full name: `\Sabre\DAV\Xml\Property\LockDiscovery`
* This class implements:
[`\Sabre\Xml\XmlSerializable`](../../../Xml/XmlSerializable.md)



## Properties


### locks

locks.

```php
public \Sabre\DAV\Locks\LockInfo[] $locks
```






***

### hideLockRoot

Hides the {DAV:}lockroot element from the response.

```php
public static bool $hideLockRoot
```

It was reported that showing the lockroot in the response can break
Office 2000 compatibility.

* This property is **static**.


***

## Methods


### __construct

__construct.

```php
public __construct(\Sabre\DAV\Locks\LockInfo[] $locks): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$locks` | **\Sabre\DAV\Locks\LockInfo[]** |  |





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


***
> Automatically generated on 2025-03-15
