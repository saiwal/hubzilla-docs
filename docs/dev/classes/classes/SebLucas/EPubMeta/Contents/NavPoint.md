***

# NavPoint

An EPUB TOC navigation point.



* Full name: `\SebLucas\EPubMeta\Contents\NavPoint`



## Properties


### id



```php
protected string $id
```






***

### class



```php
protected string $class
```






***

### playOrder



```php
protected int $playOrder
```






***

### navLabel



```php
protected string $navLabel
```






***

### contentSourceFile



```php
protected string $contentSourceFile
```






***

### contentSourceFragment



```php
protected string $contentSourceFragment
```






***

### children



```php
protected \SebLucas\EPubMeta\Contents\NavPointList $children
```






***

## Methods


### __construct



```php
public __construct(string $id, string $class, int $playOrder, string $label, string $contentSource): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** |  |
| `$class` | **string** |  |
| `$playOrder` | **int** |  |
| `$label` | **string** |  |
| `$contentSource` | **string** |  |





***

### getId



```php
public getId(): string
```












***

### getClass



```php
public getClass(): string
```












***

### getPlayOrder



```php
public getPlayOrder(): int
```












***

### getNavLabel



```php
public getNavLabel(): string
```












***

### getContentSource



```php
public getContentSource(): string
```












***

### getContentSourceFile



```php
public getContentSourceFile(): string
```












***

### getContentSourceFragment



```php
public getContentSourceFragment(): string
```












***

### getChildren



```php
public getChildren(): \SebLucas\EPubMeta\Contents\NavPointList
```












***


***
> Automatically generated on 2025-03-15
