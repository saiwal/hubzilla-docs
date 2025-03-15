
# HTMLPurifier_Token_Start

Concrete start token class.



* Full name: `\HTMLPurifier_Token_Start`
* Parent class: [`\HTMLPurifier_Token_Tag`](./HTMLPurifier_Token_Tag.md)






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












***

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


***
> Automatically generated on 2025-03-15
