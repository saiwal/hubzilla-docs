
# XML

XML Parser.

This parser parses both the xCal and xCard formats.

* Full name: `\Sabre\VObject\Parser\XML`
* Parent class: [`\Sabre\VObject\Parser\Parser`](./Parser.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`XCAL_NAMESPACE`|public| |&#039;urn:ietf:params:xml:ns:icalendar-2.0&#039;|
|`XCARD_NAMESPACE`|public| |&#039;urn:ietf:params:xml:ns:vcard-4.0&#039;|

## Properties


### input

The input data.

```php
protected array $input
```






***

### pointer

A pointer/reference to the input.

```php
private array $pointer
```






***

### root

Document, root component.

```php
protected \Sabre\VObject\Document $root
```






***

## Methods


### __construct

Creates the parser.

```php
public __construct(mixed $input = null, int $options): mixed
```

Optionally, it's possible to parse the input stream here.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |
| `$options` | **int** | any parser options (OPTION constants) |





***

### parse

Parse xCal or xCard.

```php
public parse(resource|string $input = null, int $options): \Sabre\VObject\Document
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **resource&#124;string** |  |
| `$options` | **int** |  |




**Throws:**

- [`Exception`](../../../Exception.md)



***

### parseVCalendarComponents

Parse a xCalendar component.

```php
protected parseVCalendarComponents(\Sabre\VObject\Component $parentComponent): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parentComponent` | **\Sabre\VObject\Component** |  |





***

### parseVCardComponents

Parse a xCard component.

```php
protected parseVCardComponents(\Sabre\VObject\Component $parentComponent): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parentComponent` | **\Sabre\VObject\Component** |  |





***

### parseProperties

Parse xCalendar and xCard properties.

```php
protected parseProperties(\Sabre\VObject\Component $parentComponent, string $propertyNamePrefix = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parentComponent` | **\Sabre\VObject\Component** |  |
| `$propertyNamePrefix` | **string** |  |





***

### parseComponent

Parse a component.

```php
protected parseComponent(\Sabre\VObject\Component $parentComponent): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parentComponent` | **\Sabre\VObject\Component** |  |





***

### createProperty

Create a property.

```php
protected createProperty(\Sabre\VObject\Component $parentComponent, string $name, array $parameters, string $type, mixed $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parentComponent` | **\Sabre\VObject\Component** |  |
| `$name` | **string** |  |
| `$parameters` | **array** |  |
| `$type` | **string** |  |
| `$value` | **mixed** |  |





***

### setInput

Sets the input data.

```php
public setInput(resource|string $input): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **resource&#124;string** |  |





***

### getTagName

Get tag name from a Clark notation.

```php
protected static getTagName(string $clarkedTagName): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$clarkedTagName` | **string** |  |





***


## Inherited methods


### __construct

Creates the parser.

```php
public __construct(mixed $input = null, int $options): mixed
```

Optionally, it's possible to parse the input stream here.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |
| `$options` | **int** | any parser options (OPTION constants) |





***

### parse

This method starts the parsing process.

```php
public parse(mixed $input = null, int $options): array
```

If the input was not supplied during construction, it's possible to pass
it here instead.

If either input or options are not supplied, the defaults will be used.


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |
| `$options` | **int** |  |





***

### setInput

Sets the input data.

```php
public setInput(mixed $input): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
