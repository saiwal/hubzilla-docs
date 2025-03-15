***

# Share

Share POST request parser.

This class parses the share POST request, as defined in:

http://svn.calendarserver.org/repository/calendarserver/CalendarServer/trunk/doc/Extensions/caldav-sharing.txt

* Full name: `\Sabre\CalDAV\Xml\Request\Share`
* This class implements:
[`\Sabre\Xml\XmlDeserializable`](../../../Xml/XmlDeserializable.md)



## Properties


### sharees

The list of new people added or updated or removed from the share.

```php
public \Sabre\DAV\Xml\Element\Sharee[] $sharees
```






***

## Methods


### __construct

Constructor.

```php
public __construct(\Sabre\DAV\Xml\Element\Sharee[] $sharees): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sharees` | **\Sabre\DAV\Xml\Element\Sharee[]** |  |





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
