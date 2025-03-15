
# EmphasisConverter





* Full name: `\League\HTMLToMarkdown\Converter\EmphasisConverter`
* This class implements:
[`\League\HTMLToMarkdown\Converter\ConverterInterface`](./ConverterInterface.md), [`\League\HTMLToMarkdown\ConfigurationAwareInterface`](../ConfigurationAwareInterface.md)



## Properties


### config



```php
protected \League\HTMLToMarkdown\Configuration $config
```






***

## Methods


### getNormTag



```php
protected getNormTag(?\League\HTMLToMarkdown\ElementInterface $element): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **?\League\HTMLToMarkdown\ElementInterface** |  |





***

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


***
> Automatically generated on 2025-03-15
