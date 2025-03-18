
# Toc

EPUB TOC structure for EPUB 2



* Full name: `\SebLucas\EPubMeta\Contents\Toc`



## Properties


### docTitle



```php
protected string $docTitle
```






***

### docAuthor



```php
protected string $docAuthor
```






***

### navMap



```php
protected \SebLucas\EPubMeta\Contents\NavPointList $navMap
```






***

## Methods


### __construct

Summary of __construct

```php
public __construct(string $title, string $author): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$title` | **string** |  |
| `$author` | **string** |  |





***

### getDocTitle



```php
public getDocTitle(): string
```












***

### getDocAuthor



```php
public getDocAuthor(): string
```












***

### getNavMap



```php
public getNavMap(): \SebLucas\EPubMeta\Contents\NavPointList
```












***

### findNavPointsForFile



```php
public findNavPointsForFile(string $file): array|\SebLucas\EPubMeta\Contents\NavPoint[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** |  |





***


***
> Automatically generated on 2025-03-18
