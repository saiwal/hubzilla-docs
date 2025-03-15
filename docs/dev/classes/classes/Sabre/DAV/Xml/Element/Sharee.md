***

# Sharee

This class represents the {DAV:}sharee element.



* Full name: `\Sabre\DAV\Xml\Element\Sharee`
* This class implements:
[`\Sabre\Xml\Element`](../../../Xml/Element.md)



## Properties


### href

A URL. Usually a mailto: address, could also be a principal url.

```php
public string $href
```

This uniquely identifies the sharee.




***

### principal

A local principal path. The server will do its best to locate the
principal uri based on the given uri. If we could find a local matching
principal uri, this property will contain the value.

```php
public string|null $principal
```






***

### properties

A list of WebDAV properties that describe the sharee. This might for
example contain a {DAV:}displayname with the real name of the user.

```php
public array $properties
```






***

### access

Share access level. One of the Sabre\DAV\Sharing\Plugin::ACCESS
constants.

```php
public int $access
```

Can be one of:

ACCESS_READ
ACCESS_READWRITE
ACCESS_SHAREDOWNER
ACCESS_NOACCESS

depending on context.




***

### comment

When a sharee is originally invited to a share, the sharer may add
a comment. This will be placed in this property.

```php
public string $comment
```






***

### inviteStatus

The status of the invite, should be one of the
Sabre\DAV\Sharing\Plugin::INVITE constants.

```php
public int $inviteStatus
```






***

## Methods


### __construct

Creates the object.

```php
public __construct(array $properties = []): mixed
```

$properties will be used to populate all internal properties.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$properties` | **array** |  |





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

### xmlDeserialize

The deserialize method is called during xml parsing.

```php
public static xmlDeserialize(\Sabre\Xml\Reader $reader): mixed
```

This method is called statically, this is because in theory this method
may be used as a type of constructor, or factory method.

Often you want to return an instance of the current class, but you are
free to return other data as well.

You are responsible for advancing the reader to the next element. Not
doing anything will result in a never-ending loop.

If you just want to skip parsing for this element altogether, you can
just call $reader->next();

$reader->parseInnerTree() will parse the entire sub-tree, and advance to
the next element.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reader` | **\Sabre\Xml\Reader** |  |





***


***
> Automatically generated on 2025-03-15
