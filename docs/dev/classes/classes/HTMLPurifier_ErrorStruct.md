***

# HTMLPurifier_ErrorStruct

Records errors for particular segments of an HTML document such as tokens,
attributes or CSS properties. They can contain error structs (which apply
to components of what they represent), but their main purpose is to hold
errors applying to whatever struct is being used.



* Full name: `\HTMLPurifier_ErrorStruct`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`TOKEN`|public| |0|
|`ATTR`|public| |1|
|`CSSPROP`|public| |2|

## Properties


### type

Type of this struct.

```php
public $type
```






***

### value

Value of the struct we are recording errors for. There are various
values for this:
 - TOKEN: Instance of HTMLPurifier_Token
 - ATTR: array('attr-name', 'value')
 - CSSPROP: array('prop-name', 'value')

```php
public $value
```






***

### errors

Errors registered for this structure.

```php
public $errors
```






***

### children

Child ErrorStructs that are from this structure. For example, a TOKEN
ErrorStruct would contain ATTR ErrorStructs. This is a multi-dimensional
array in structure: [TYPE]['identifier']

```php
public $children
```






***

## Methods


### getChild



```php
public getChild(string $type, string $id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** |  |
| `$id` | **string** |  |





***

### addError



```php
public addError(int $severity, string $message): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$severity` | **int** |  |
| `$message` | **string** |  |





***


***
> Automatically generated on 2025-03-15
