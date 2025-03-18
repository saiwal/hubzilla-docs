
# Caption

Handles `<media:text>` captions as defined in Media RSS.

Used by {@see \SimplePie\Enclosure::get_caption()} and {@see \SimplePie\Enclosure::get_captions()}

This class can be overloaded with {@see \SimplePie\SimplePie::set_caption_class()}

* Full name: `\SimplePie\Caption`



## Properties


### type

Content type

```php
public string $type
```





**See Also:**

* \SimplePie\get_type() - 

***

### lang

Language

```php
public string $lang
```





**See Also:**

* \SimplePie\get_language() - 

***

### startTime

Start time

```php
public string $startTime
```





**See Also:**

* \SimplePie\get_starttime() - 

***

### endTime

End time

```php
public string $endTime
```





**See Also:**

* \SimplePie\get_endtime() - 

***

### text

Caption text

```php
public string $text
```





**See Also:**

* \SimplePie\get_text() - 

***

## Methods


### __construct

Constructor, used to input the data

```php
public __construct(mixed $type = null, mixed $lang = null, mixed $startTime = null, mixed $endTime = null, mixed $text = null): mixed
```

For documentation on all the parameters, see the corresponding
properties and their accessors






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **mixed** |  |
| `$lang` | **mixed** |  |
| `$startTime` | **mixed** |  |
| `$endTime` | **mixed** |  |
| `$text` | **mixed** |  |





***

### __toString

String-ified version

```php
public __toString(): string
```












***

### get_endtime

Get the end time

```php
public get_endtime(): string|null
```









**Return Value:**

Time in the format 'hh:mm:ss.SSS'




***

### get_language

Get the language

```php
public get_language(): string|null
```









**Return Value:**

Language code as per RFC 3066




**See Also:**

* http://tools.ietf.org/html/rfc3066 - 

***

### get_starttime

Get the start time

```php
public get_starttime(): string|null
```









**Return Value:**

Time in the format 'hh:mm:ss.SSS'




***

### get_text

Get the text of the caption

```php
public get_text(): string|null
```












***

### get_type

Get the content type (not MIME type)

```php
public get_type(): string|null
```









**Return Value:**

Either 'text' or 'html'




***


***
> Automatically generated on 2025-03-18
