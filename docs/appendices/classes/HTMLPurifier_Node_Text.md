
# HTMLPurifier_Node_Text

Concrete text token class.

Text tokens comprise of regular parsed character data (PCDATA) and raw
character data (from the CDATA sections). Internally, their
data is parsed with all entities expanded. Surprisingly, the text token
does have a "tag name" called #PCDATA, which is how the DTD represents it
in permissible child nodes.

* Full name: `\HTMLPurifier_Node_Text`
* Parent class: [`\HTMLPurifier_Node`](./HTMLPurifier_Node.md)



## Properties


### name

PCDATA tag name compatible with DTD, see
HTMLPurifier_ChildDef_Custom for details.

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
public __construct(string $data, mixed $is_whitespace, int $line = null, int $col = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | String parsed character data. |
| `$is_whitespace` | **mixed** |  |
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
> Automatically generated on 2025-03-18
