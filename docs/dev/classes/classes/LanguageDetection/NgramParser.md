***

# NgramParser

Class NgramParser



* Full name: `\LanguageDetection\NgramParser`
* This class is an **Abstract class**



## Properties


### minLength



```php
protected int $minLength
```






***

### maxLength



```php
protected int $maxLength
```






***

### maxNgrams



```php
protected int $maxNgrams
```






***

### tokenizer



```php
protected \LanguageDetection\Tokenizer\TokenizerInterface $tokenizer
```






***

## Methods


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
