
# HTMLPurifier_Token

Abstract base token class that all others inherit from.



* Full name: `\HTMLPurifier_Token`
* This class is an **Abstract class**



## Properties


### line

Line number node was on in source document. Null if unknown.

```php
public $line
```






***

### col

Column of line node was on in source document. Null if unknown.

```php
public $col
```






***

### armor

Lookup array of processing that this token is exempt from.

```php
public $armor
```

Currently, valid values are "ValidateAttributes" and
"MakeWellFormed_TagClosedError"




***

### skip

Used during MakeWellFormed.  See Note [Injector skips]

```php
public $skip
```






***

### rewind



```php
public $rewind
```






***

### carryover



```php
public $carryover
```






***

## Methods


### __get



```php
public __get(string $n): null|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$n` | **string** |  |





***

### position

Sets the position of the token in the source document.

```php
public position(int $l = null, int $c = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$l` | **int** |  |
| `$c` | **int** |  |





***

### rawPosition

Convenience function for DirectLex settings line/col position.

```php
public rawPosition(int $l, int $c): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$l` | **int** |  |
| `$c` | **int** |  |





***

### toNode

Converts a token into its corresponding node.

```php
public toNode(): mixed
```




* This method is **abstract**.







***


***
> Automatically generated on 2025-03-18
