
# HTMLPurifier_Token_Text

Concrete text token class.

Text tokens comprise of regular parsed character data (PCDATA) and raw
character data (from the CDATA sections). Internally, their
data is parsed with all entities expanded. Surprisingly, the text token
does have a "tag name" called #PCDATA, which is how the DTD represents it
in permissible child nodes.

* Full name: `\HTMLPurifier_Token_Text`
* Parent class: [`\HTMLPurifier_Token`](./HTMLPurifier_Token.md)



## Properties


### name



```php
public $name
```






***

### data



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

Constructor, accepts data and determines if it is whitespace.

```php
public __construct(string $data, int $line = null, int $col = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | String parsed character data. |
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
