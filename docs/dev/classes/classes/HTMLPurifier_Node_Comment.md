
# HTMLPurifier_Node_Comment

Concrete comment node class.



* Full name: `\HTMLPurifier_Node_Comment`
* Parent class: [`\HTMLPurifier_Node`](./HTMLPurifier_Node.md)



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
