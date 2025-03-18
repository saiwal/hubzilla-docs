
# ParagraphConverter





* Full name: `\League\HTMLToMarkdown\Converter\ParagraphConverter`
* This class implements:
[`\League\HTMLToMarkdown\Converter\ConverterInterface`](./ConverterInterface.md)




## Methods


### convert



```php
public convert(\League\HTMLToMarkdown\ElementInterface $element): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\League\HTMLToMarkdown\ElementInterface** |  |





***

### getSupportedTags



```php
public getSupportedTags(): string[]
```












***

### escapeSpecialCharacters



```php
private escapeSpecialCharacters(string $line): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$line` | **string** |  |





***

### escapeFirstCharacters



```php
private escapeFirstCharacters(string $line): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$line` | **string** |  |





***

### escapeOtherCharacters



```php
private escapeOtherCharacters(string $line): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$line` | **string** |  |





***

### escapeOtherCharactersRegex



```php
private escapeOtherCharactersRegex(string $line): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$line` | **string** |  |





***


***
> Automatically generated on 2025-03-18
