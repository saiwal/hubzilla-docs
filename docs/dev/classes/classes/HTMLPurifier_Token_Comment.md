
# HTMLPurifier_Token_Comment

Concrete comment token class. Generally will be ignored.



* Full name: `\HTMLPurifier_Token_Comment`
* Parent class: [`\HTMLPurifier_Token`](./HTMLPurifier_Token.md)



## Properties


### data

Character data within comment.

```php
public $data
```






***

### is_whitespace



```php
public $is_whitespace
```






***

## Methods


### __construct

Transparent constructor.

```php
public __construct(string $data, int $line = null, int $col = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | String comment data. |
| `$line` | **int** |  |
| `$col` | **int** |  |





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
> Automatically generated on 2025-03-15
