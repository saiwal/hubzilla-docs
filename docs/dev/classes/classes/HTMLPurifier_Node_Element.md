***

# HTMLPurifier_Node_Element

Concrete element node class.



* Full name: `\HTMLPurifier_Node_Element`
* Parent class: [`\HTMLPurifier_Node`](./HTMLPurifier_Node.md)



## Properties


### name

The lower-case name of the tag, like 'a', 'b' or 'blockquote'.

```php
public $name
```






***

### attr

Associative array of the node's attributes.

```php
public $attr
```






***

### children

List of child elements.

```php
public $children
```






***

### empty

Does this use the <a></a> form or the </a> form, i.e.

```php
public $empty
```

is it a pair of start/end tokens or an empty token.




***

### endCol



```php
public $endCol
```






***

### endLine



```php
public $endLine
```






***

### endArmor



```php
public $endArmor
```






***

## Methods


### __construct



```php
public __construct(mixed $name, mixed $attr = array(), mixed $line = null, mixed $col = null, mixed $armor = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |
| `$attr` | **mixed** |  |
| `$line` | **mixed** |  |
| `$col` | **mixed** |  |
| `$armor` | **mixed** |  |





***

### toTokenPair

Returns a pair of start and end tokens, where the end token
is null if it is not necessary. Does not include children.

```php
public toTokenPair(): mixed
```












***


## Inherited methods


### toTokenPair

Returns a pair of start and end tokens, where the end token
is null if it is not necessary. Does not include children.

```php
public toTokenPair(): mixed
```




* This method is **abstract**.







***


***
> Automatically generated on 2025-03-15
