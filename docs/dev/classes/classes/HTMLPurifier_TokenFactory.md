
# HTMLPurifier_TokenFactory

Factory for token generation.



* Full name: `\HTMLPurifier_TokenFactory`



## Properties


### p_start



```php
private $p_start
```






***

### p_end



```php
private $p_end
```






***

### p_empty



```php
private $p_empty
```






***

### p_text



```php
private $p_text
```






***

### p_comment



```php
private $p_comment
```






***

## Methods


### __construct

Generates blank prototypes for cloning.

```php
public __construct(): mixed
```












***

### createStart

Creates a HTMLPurifier_Token_Start.

```php
public createStart(string $name, array $attr = array()): \HTMLPurifier_Token_Start
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Tag name |
| `$attr` | **array** | Associative array of attributes |


**Return Value:**

Generated HTMLPurifier_Token_Start




***

### createEnd

Creates a HTMLPurifier_Token_End.

```php
public createEnd(string $name): \HTMLPurifier_Token_End
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Tag name |


**Return Value:**

Generated HTMLPurifier_Token_End




***

### createEmpty

Creates a HTMLPurifier_Token_Empty.

```php
public createEmpty(string $name, array $attr = array()): \HTMLPurifier_Token_Empty
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Tag name |
| `$attr` | **array** | Associative array of attributes |


**Return Value:**

Generated HTMLPurifier_Token_Empty




***

### createText

Creates a HTMLPurifier_Token_Text.

```php
public createText(string $data): \HTMLPurifier_Token_Text
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | Data of text token |


**Return Value:**

Generated HTMLPurifier_Token_Text




***

### createComment

Creates a HTMLPurifier_Token_Comment.

```php
public createComment(string $data): \HTMLPurifier_Token_Comment
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | Data of comment token |


**Return Value:**

Generated HTMLPurifier_Token_Comment




***


***
> Automatically generated on 2025-03-15
