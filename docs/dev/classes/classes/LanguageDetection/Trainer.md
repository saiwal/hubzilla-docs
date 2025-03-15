
# Trainer

Class Trainer



* Full name: `\LanguageDetection\Trainer`
* Parent class: [`\LanguageDetection\NgramParser`](./NgramParser.md)




## Methods


### learn

Generates language profiles for all language files

```php
public learn(string $dirname = &#039;&#039;): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dirname` | **string** | Name of the directory where the translations files are located |





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
