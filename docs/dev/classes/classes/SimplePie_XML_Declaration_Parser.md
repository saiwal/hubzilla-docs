***

# SimplePie_XML_Declaration_Parser

Parses the XML Declaration



* Full name: `\SimplePie_XML_Declaration_Parser`
* Parent class: [`\SimplePie\XML\Declaration\Parser`](./SimplePie/XML/Declaration/Parser.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


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
public parse(): bool
```









**Return Value:**

true on success, false on failure




***

### has_data

Check whether there is data beyond the pointer

```php
public has_data(): bool
```









**Return Value:**

true if there is further data, false if not




***

### skip_whitespace

Advance past any whitespace

```php
public skip_whitespace(): int
```









**Return Value:**

Number of whitespace characters passed




***

### get_value

Read value

```php
public get_value(): mixed
```












***

### before_version_name



```php
public before_version_name(): mixed
```












***

### version_name



```php
public version_name(): mixed
```












***

### version_equals



```php
public version_equals(): mixed
```












***

### version_value



```php
public version_value(): mixed
```












***

### encoding_name



```php
public encoding_name(): mixed
```












***

### encoding_equals



```php
public encoding_equals(): mixed
```












***

### encoding_value



```php
public encoding_value(): mixed
```












***

### standalone_name



```php
public standalone_name(): mixed
```












***

### standalone_equals



```php
public standalone_equals(): mixed
```












***

### standalone_value



```php
public standalone_value(): mixed
```












***


***
> Automatically generated on 2025-03-15
