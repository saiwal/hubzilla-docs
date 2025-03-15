
# StopWords

Phonetic-Helper-Class



* Full name: `\voku\helper\StopWords`
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**



## Properties


### availableLanguages



```php
private static array $availableLanguages
```



* This property is **static**.


***

### stopWords



```php
private array $stopWords
```






***

## Methods


### loadLanguageData

Load language-data from one language.

```php
private loadLanguageData(string $language = &#039;de&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$language` | **string** |  |




**Throws:**

- [`StopWordsLanguageNotExists`](./StopWordsLanguageNotExists.md)



***

### getData

Get data from "/data/*.php".

```php
private getData(string $file): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** |  |


**Return Value:**

<p>Will return an empty array on error.</p>




***

### getStopWordsFromLanguage

Get the stop-words from one language.

```php
public getStopWordsFromLanguage(string $language = &#039;de&#039;): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$language` | **string** |  |




**Throws:**

- [`StopWordsLanguageNotExists`](./StopWordsLanguageNotExists.md)



***

### loadLanguageDataAll



```php
private loadLanguageDataAll(): mixed
```












***

### getStopWordsAll

Get all stop-words from all languages.

```php
public getStopWordsAll(): array
```











**Throws:**

- [`StopWordsLanguageNotExists`](./StopWordsLanguageNotExists.md)



***


***
> Automatically generated on 2025-03-15
