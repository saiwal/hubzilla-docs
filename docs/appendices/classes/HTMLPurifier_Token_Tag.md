
# HTMLPurifier_Token_Tag

Abstract class of a tag token (start, end or empty), and its behavior.



* Full name: `\HTMLPurifier_Token_Tag`
* Parent class: [`\HTMLPurifier_Token`](./HTMLPurifier_Token.md)
* This class is an **Abstract class**



## Properties


### is_tag

Static bool marker that indicates the class is a tag.

```php
public $is_tag
```

This allows us to check objects with <tt>!empty($obj->is_tag)</tt>
without having to use a function call <tt>is_a()</tt>.




***

### name

The lower-case name of the tag, like 'a', 'b' or 'blockquote'.

```php
public $name
```






***

### attr

Associative array of the tag's attributes.

```php
public $attr
```






***

## Methods


### __construct

Non-overloaded constructor, which lower-cases passed tag name.

```php
public __construct(string $name, array $attr = array(), int $line = null, int $col = null, array $armor = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | String name. |
| `$attr` | **array** | Associative array of attributes. |
| `$line` | **int** |  |
| `$col` | **int** |  |
| `$armor` | **array** |  |





***

### toNode

Converts a token into its corresponding node.

```php
public toNode(): mixed
```












***


## Inherited methods


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
