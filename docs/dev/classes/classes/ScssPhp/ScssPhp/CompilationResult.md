***

# CompilationResult





* Full name: `\ScssPhp\ScssPhp\CompilationResult`



## Properties


### css



```php
private string $css
```






***

### sourceMap



```php
private string|null $sourceMap
```






***

### includedFiles



```php
private string[] $includedFiles
```






***

## Methods


### __construct



```php
public __construct(string $css, string|null $sourceMap, string[] $includedFiles): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$css` | **string** |  |
| `$sourceMap` | **string&#124;null** |  |
| `$includedFiles` | **string[]** |  |





***

### getCss



```php
public getCss(): string
```












***

### getIncludedFiles



```php
public getIncludedFiles(): string[]
```












***

### getSourceMap

The sourceMap content, if it was generated

```php
public getSourceMap(): null|string
```












***


***
> Automatically generated on 2025-03-15
