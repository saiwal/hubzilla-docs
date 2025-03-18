
# LinkConverter





* Full name: `\League\HTMLToMarkdown\Converter\LinkConverter`
* This class implements:
[`\League\HTMLToMarkdown\Converter\ConverterInterface`](./ConverterInterface.md), [`\League\HTMLToMarkdown\ConfigurationAwareInterface`](../ConfigurationAwareInterface.md)



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

### isValidAutolink



```php
private isValidAutolink(string $href): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$href` | **string** |  |





***

### isValidEmail



```php
private isValidEmail(string $email): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$email` | **string** |  |





***

### shouldStrip



```php
private shouldStrip(): bool
```












***


***
> Automatically generated on 2025-03-18
