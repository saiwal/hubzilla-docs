***

# VCard

Splitter.

This class is responsible for splitting up VCard objects.

It is assumed that the input stream contains 1 or more VCARD objects. This
class checks for BEGIN:VCARD and END:VCARD and parses each encountered
component individually.

* Full name: `\Sabre\VObject\Splitter\VCard`
* This class implements:
[`\Sabre\VObject\Splitter\SplitterInterface`](./SplitterInterface.md)



## Properties


### input

File handle.

```php
protected resource $input
```






***

### parser

Persistent parser.

```php
protected \Sabre\VObject\Parser\MimeDir $parser
```






***

## Methods


### __construct

Constructor.

```php
public __construct(resource $input, int $options): mixed
```

The splitter should receive an readable file stream as its input.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **resource** |  |
| `$options` | **int** | parser options, see the OPTIONS constants |





***

### getNext

Every time getNext() is called, a new object will be parsed, until we
hit the end of the stream.

```php
public getNext(): \Sabre\VObject\Component|null
```

When the end is reached, null will be returned.










***


***
> Automatically generated on 2025-03-15
