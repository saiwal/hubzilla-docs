***

# SimplePie_Caption

Handles `<media:text>` captions as defined in Media RSS.



* Full name: `\SimplePie_Caption`
* Parent class: [`\SimplePie\Caption`](./SimplePie/Caption.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


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
> Automatically generated on 2025-03-15
