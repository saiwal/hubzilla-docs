
# Environment





* Full name: `\League\HTMLToMarkdown\Environment`
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**



## Properties


### config



```php
protected \League\HTMLToMarkdown\Configuration $config
```






***

### converters



```php
protected \League\HTMLToMarkdown\Converter\ConverterInterface[] $converters
```






***

## Methods


### __construct



```php
public __construct(array&lt;string,mixed&gt; $config = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **array<string,mixed>** |  |





***

### getConfig



```php
public getConfig(): \League\HTMLToMarkdown\Configuration
```












***

### addConverter



```php
public addConverter(\League\HTMLToMarkdown\Converter\ConverterInterface $converter): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$converter` | **\League\HTMLToMarkdown\Converter\ConverterInterface** |  |





***

### getConverterByTag



```php
public getConverterByTag(string $tag): \League\HTMLToMarkdown\Converter\ConverterInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **string** |  |





***

### createDefaultEnvironment



```php
public static createDefaultEnvironment(array&lt;string,mixed&gt; $config = []): \League\HTMLToMarkdown\Environment
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **array<string,mixed>** |  |





***


***
> Automatically generated on 2025-03-18
