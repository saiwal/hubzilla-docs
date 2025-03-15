
# HTMLPurifier_Filter_ExtractStyleBlocks

This filter extracts <style> blocks from input HTML, cleans them up
using CSSTidy, and then places them in $purifier->context->get('StyleBlocks')
so they can be used elsewhere in the document.



* Full name: `\HTMLPurifier_Filter_ExtractStyleBlocks`
* Parent class: [`\HTMLPurifier_Filter`](./HTMLPurifier_Filter.md)



## Properties


### name

Name of the filter for identification purposes.

```php
public $name
```






***

### _styleMatches



```php
private $_styleMatches
```






***

### _tidy



```php
private $_tidy
```






***

### _id_attrdef



```php
private $_id_attrdef
```






***

### _class_attrdef



```php
private $_class_attrdef
```






***

### _enum_attrdef



```php
private $_enum_attrdef
```






***

## Methods


### __construct



```php
public __construct(): mixed
```












***

### styleCallback

Save the contents of CSS blocks to style matches

```php
protected styleCallback(array $matches): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** | preg_replace style $matches array |





***

### preFilter

Removes inline <style> tags from HTML, saves them for later use

```php
public preFilter(string $html, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***

### cleanCSS

Takes CSS (the stuff found in <style>) and cleans it.

```php
public cleanCSS(string $css, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$css` | **string** | CSS styling to clean |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |


**Return Value:**

Cleaned CSS



**Throws:**

- [`HTMLPurifier_Exception`](./HTMLPurifier_Exception.md)



***


## Inherited methods


### preFilter

Pre-processor function, handles HTML before HTML Purifier

```php
public preFilter(string $html, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***

### postFilter

Post-processor function, handles HTML after HTML Purifier

```php
public postFilter(string $html, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***


***
> Automatically generated on 2025-03-15
