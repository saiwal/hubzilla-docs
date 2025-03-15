
# HTML5





* Full name: `\HTML5`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`PCDATA`|public| |0|
|`RCDATA`|public| |1|
|`CDATA`|public| |2|
|`PLAINTEXT`|public| |3|
|`DOCTYPE`|public| |0|
|`STARTTAG`|public| |1|
|`ENDTAG`|public| |2|
|`COMMENT`|public| |3|
|`CHARACTR`|public| |4|
|`EOF`|public| |5|

## Properties


### data



```php
private $data
```






***

### char



```php
private $char
```






***

### EOF



```php
private $EOF
```






***

### state



```php
private $state
```






***

### tree



```php
private $tree
```






***

### token



```php
private $token
```






***

### content_model



```php
private $content_model
```






***

### escape



```php
private $escape
```






***

### entities



```php
private $entities
```






***

## Methods


### __construct



```php
public __construct(mixed $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |





***

### save



```php
public save(): mixed
```












***

### char



```php
private char(): mixed
```












***

### character



```php
private character(mixed $s, mixed $l): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$s` | **mixed** |  |
| `$l` | **mixed** |  |





***

### characters



```php
private characters(mixed $char_class, mixed $start): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$char_class` | **mixed** |  |
| `$start` | **mixed** |  |





***

### dataState



```php
private dataState(): mixed
```












***

### entityDataState



```php
private entityDataState(): mixed
```












***

### tagOpenState



```php
private tagOpenState(): mixed
```












***

### closeTagOpenState



```php
private closeTagOpenState(): mixed
```












***

### tagNameState



```php
private tagNameState(): mixed
```












***

### beforeAttributeNameState



```php
private beforeAttributeNameState(): mixed
```












***

### attributeNameState



```php
private attributeNameState(): mixed
```












***

### afterAttributeNameState



```php
private afterAttributeNameState(): mixed
```












***

### beforeAttributeValueState



```php
private beforeAttributeValueState(): mixed
```












***

### attributeValueDoubleQuotedState



```php
private attributeValueDoubleQuotedState(): mixed
```












***

### attributeValueSingleQuotedState



```php
private attributeValueSingleQuotedState(): mixed
```












***

### attributeValueUnquotedState



```php
private attributeValueUnquotedState(): mixed
```












***

### entityInAttributeValueState



```php
private entityInAttributeValueState(): mixed
```












***

### bogusCommentState



```php
private bogusCommentState(): mixed
```












***

### markupDeclarationOpenState



```php
private markupDeclarationOpenState(): mixed
```












***

### commentState



```php
private commentState(): mixed
```












***

### commentDashState



```php
private commentDashState(): mixed
```












***

### commentEndState



```php
private commentEndState(): mixed
```












***

### doctypeState



```php
private doctypeState(): mixed
```












***

### beforeDoctypeNameState



```php
private beforeDoctypeNameState(): mixed
```












***

### doctypeNameState



```php
private doctypeNameState(): mixed
```












***

### afterDoctypeNameState



```php
private afterDoctypeNameState(): mixed
```












***

### bogusDoctypeState



```php
private bogusDoctypeState(): mixed
```












***

### entity



```php
private entity(): mixed
```












***

### emitToken



```php
private emitToken(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### EOF



```php
private EOF(): mixed
```












***


***
> Automatically generated on 2025-03-15
