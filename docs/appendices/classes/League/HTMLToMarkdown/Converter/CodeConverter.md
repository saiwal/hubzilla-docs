
# CodeConverter





* Full name: `\League\HTMLToMarkdown\Converter\CodeConverter`
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

### shouldBeBlock



```php
private shouldBeBlock(\League\HTMLToMarkdown\ElementInterface $element, string $code): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\League\HTMLToMarkdown\ElementInterface** |  |
| `$code` | **string** |  |





***


***
> Automatically generated on 2025-03-18
