
# TableConverter





* Full name: `\League\HTMLToMarkdown\Converter\TableConverter`
* This class implements:
[`\League\HTMLToMarkdown\Converter\ConverterInterface`](./ConverterInterface.md), [`\League\HTMLToMarkdown\PreConverterInterface`](../PreConverterInterface.md), [`\League\HTMLToMarkdown\ConfigurationAwareInterface`](../ConfigurationAwareInterface.md)



## Properties


### config



```php
protected \League\HTMLToMarkdown\Configuration $config
```






***

### alignments



```php
private static array&lt;string,string&gt; $alignments
```



* This property is **static**.


***

### columnAlignments



```php
private array&lt;int,string&gt;|null $columnAlignments
```






***

### caption



```php
private string|null $caption
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

### preConvert



```php
public preConvert(\League\HTMLToMarkdown\ElementInterface $element): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\League\HTMLToMarkdown\ElementInterface** |  |





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
> Automatically generated on 2025-03-18
