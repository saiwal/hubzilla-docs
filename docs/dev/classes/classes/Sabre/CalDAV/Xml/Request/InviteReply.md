
# InviteReply

Invite-reply POST request parser.

This class parses the invite-reply POST request, as defined in:

http://svn.calendarserver.org/repository/calendarserver/CalendarServer/trunk/doc/Extensions/caldav-sharing.txt

* Full name: `\Sabre\CalDAV\Xml\Request\InviteReply`
* This class implements:
[`\Sabre\Xml\XmlDeserializable`](../../../Xml/XmlDeserializable.md)



## Properties


### href

The sharee calendar user address.

```php
public string $href
```

This is the address that the original invite was set to




***

### calendarUri

The uri to the calendar that was being shared.

```php
public string $calendarUri
```






***

### inReplyTo

The id of the invite message that's being responded to.

```php
public string $inReplyTo
```






***

### summary

An optional message.

```php
public string $summary
```






***

### status

Either SharingPlugin::STATUS_ACCEPTED or SharingPlugin::STATUS_DECLINED.

```php
public int $status
```






***

## Methods


### __construct

Constructor.

```php
public __construct(string $href, string $calendarUri, string $inReplyTo, string $summary, int $status): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$href` | **string** |  |
| `$calendarUri` | **string** |  |
| `$inReplyTo` | **string** |  |
| `$summary` | **string** |  |
| `$status` | **int** |  |





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
