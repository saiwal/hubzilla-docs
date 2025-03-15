
# SyncCollectionReport

SyncCollection request parser.

This class parses the {DAV:}sync-collection reprot, as defined in:

http://tools.ietf.org/html/rfc6578#section-3.2

* Full name: `\Sabre\DAV\Xml\Request\SyncCollectionReport`
* This class implements:
[`\Sabre\Xml\XmlDeserializable`](../../../Xml/XmlDeserializable.md)



## Properties


### syncToken

The sync-token the client supplied for the report.

```php
public string|null $syncToken
```






***

### syncLevel

The 'depth' of the sync the client is interested in.

```php
public int $syncLevel
```






***

### limit

Maximum amount of items returned.

```php
public int|null $limit
```






***

### properties

The list of properties that are being requested for every change.

```php
public array|null $properties
```






***

## Methods


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
