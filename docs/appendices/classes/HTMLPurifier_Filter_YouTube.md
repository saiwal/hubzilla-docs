
# HTMLPurifier_Filter_YouTube

Represents a pre or post processing filter on HTML Purifier's output

Sometimes, a little ad-hoc fixing of HTML has to be done before
it gets sent through HTML Purifier: you can use filters to acheive
this effect. For instance, YouTube videos can be preserved using
this manner. You could have used a decorator for this task, but
PHP's support for them is not terribly robust, so we're going
to just loop through the filters.

Filters should be exited first in, last out. If there are three filters,
named 1, 2 and 3, the order of execution should go 1->preFilter,
2->preFilter, 3->preFilter, purify, 3->postFilter, 2->postFilter,
1->postFilter.

* Full name: `\HTMLPurifier_Filter_YouTube`
* Parent class: [`\HTMLPurifier_Filter`](./HTMLPurifier_Filter.md)



## Properties


### name

Name of the filter for identification purposes.

```php
public $name
```






***

## Methods


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

### armorUrl



```php
protected armorUrl(mixed $url): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### postFilterCallback



```php
protected postFilterCallback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





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
> Automatically generated on 2025-03-18
