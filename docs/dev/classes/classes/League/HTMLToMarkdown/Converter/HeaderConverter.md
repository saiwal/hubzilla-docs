***

# HeaderConverter





* Full name: `\League\HTMLToMarkdown\Converter\HeaderConverter`
* This class implements:
[`\League\HTMLToMarkdown\Converter\ConverterInterface`](./ConverterInterface.md), [`\League\HTMLToMarkdown\ConfigurationAwareInterface`](../ConfigurationAwareInterface.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`STYLE_ATX`|public| |&#039;atx&#039;|
|`STYLE_SETEXT`|public| |&#039;setext&#039;|

## Properties


### config



```php
protected \League\HTMLToMarkdown\Configuration $config
```






***

## Methods


### setConfig



```php
public setConfig(\League\HTMLToMarkdown\Configuration $config): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\League\HTMLToMarkdown\Configuration** |  |





***

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

### createSetextHeader



```php
private createSetextHeader(int $level, string $content): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$level` | **int** |  |
| `$content` | **string** |  |





***

### createAtxHeader



```php
private createAtxHeader(int $level, string $content): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$level` | **int** |  |
| `$content` | **string** |  |





***


***
> Automatically generated on 2025-03-15
