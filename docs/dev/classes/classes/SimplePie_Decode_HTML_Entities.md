***

# SimplePie_Decode_HTML_Entities

Decode HTML Entities

This implements HTML5 as of revision 967 (2007-06-28)

* Full name: `\SimplePie_Decode_HTML_Entities`
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.



## Properties


### data

Data to be parsed

```php
public string $data
```






***

### consumed

Currently consumed bytes

```php
public string $consumed
```






***

### position

Position of the current byte being parsed

```php
public int $position
```






***

## Methods


### __construct

Create an instance of the class with the input data

```php
public __construct(string $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | Input data |





***

### parse

Parse the input data

```php
public parse(): string
```









**Return Value:**

Output data




***

### consume

Consume the next byte

```php
public consume(): mixed
```









**Return Value:**

The next byte, or false, if there is no more data




***

### consume_range

Consume a range of characters

```php
public consume_range(string $chars): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$chars` | **string** | Characters to consume |


**Return Value:**

A series of characters that match the range, or false




***

### unconsume

Unconsume one byte

```php
public unconsume(): mixed
```












***

### entity

Decode an entity

```php
public entity(): mixed
```












***


***
> Automatically generated on 2025-03-15
