
# Language

Class Language



* Full name: `\LanguageDetection\Language`
* Parent class: [`\LanguageDetection\NgramParser`](./NgramParser.md)



## Properties


### tokens



```php
protected array&lt;string,array&lt;string,int&gt;&gt; $tokens
```






***

## Methods


### __construct

Loads all language files

```php
public __construct(array $lang = [], string $dirname = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lang` | **array** | List of ISO 639-1 codes, that should be used in the detection phase |
| `$dirname` | **string** | Name of the directory where the translations files are located |





***

### detect

Detects the language from a given text string

```php
public detect(string $str): \LanguageDetection\LanguageResult
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |





***


## Inherited methods


### setMinLength



```php
public setMinLength(int $minLength): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$minLength` | **int** |  |




**Throws:**

- [`LengthException`](../LengthException.md)



***

### setMaxLength



```php
public setMaxLength(int $maxLength): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$maxLength` | **int** |  |




**Throws:**

- [`LengthException`](../LengthException.md)



***

### setMaxNgrams



```php
public setMaxNgrams(int $maxNgrams): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$maxNgrams` | **int** |  |




**Throws:**

- [`LengthException`](../LengthException.md)



***

### setTokenizer

Sets the tokenizer

```php
public setTokenizer(\LanguageDetection\Tokenizer\TokenizerInterface $tokenizer): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tokenizer` | **\LanguageDetection\Tokenizer\TokenizerInterface** |  |





***

### tokenize



```php
private tokenize(string $str): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |





***

### getNgrams



```php
protected getNgrams(string $str): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |





***


***
> Automatically generated on 2025-03-15
