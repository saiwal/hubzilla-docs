
# HTMLPurifier

Facade that coordinates HTML Purifier's subsystems in order to purify HTML.



* Full name: `\HTMLPurifier`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`VERSION`|public| |&#039;4.17.0&#039;|

## Properties


### version

Version of HTML Purifier.

```php
public $version
```






***

### config

Global configuration object.

```php
public $config
```






***

### filters

Array of extra filter objects to run on HTML,
for backwards compatibility.

```php
private $filters
```






***

### instance

Single instance of HTML Purifier.

```php
private static $instance
```



* This property is **static**.


***

### strategy



```php
protected $strategy
```






***

### generator



```php
protected $generator
```






***

### context

Resultant context of last run purification.

```php
public $context
```

Is an array of contexts if the last called method was purifyArray().




***

## Methods


### __construct

Initializes the purifier.

```php
public __construct(\HTMLPurifier_Config|mixed $config = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config&#124;mixed** | Optional HTMLPurifier_Config object<br />for all instances of the purifier, if omitted, a default<br />configuration is supplied (which can be overridden on a<br />per-use basis).<br />The parameter can also be any type that<br />HTMLPurifier_Config::create() supports. |





***

### addFilter

Adds a filter to process the output. First come first serve

```php
public addFilter(\HTMLPurifier_Filter $filter): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filter` | **\HTMLPurifier_Filter** | HTMLPurifier_Filter object |





***

### purify

Filters an HTML snippet/document to be XSS-free and standards-compliant.

```php
public purify(string $html, \HTMLPurifier_Config $config = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string** | String of HTML to purify |
| `$config` | **\HTMLPurifier_Config** | Config object for this operation,<br />if omitted, defaults to the config object specified during this<br />object&#039;s construction. The parameter can also be any type<br />that HTMLPurifier_Config::create() supports. |


**Return Value:**

Purified HTML




***

### purifyArray

Filters an array of HTML snippets

```php
public purifyArray(string[] $array_of_html, \HTMLPurifier_Config $config = null): string[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array_of_html` | **string[]** | Array of html snippets |
| `$config` | **\HTMLPurifier_Config** | Optional config object for this operation.<br />See HTMLPurifier::purify() for more details. |


**Return Value:**

Array of purified HTML




***

### instance

Singleton for enforcing just one HTML Purifier in your system

```php
public static instance(\HTMLPurifier|\HTMLPurifier_Config $prototype = null): \HTMLPurifier
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prototype` | **\HTMLPurifier&#124;\HTMLPurifier_Config** | Optional prototype<br />HTMLPurifier instance to overload singleton with,<br />or HTMLPurifier_Config instance to configure the<br />generated version with. |





***

### getInstance

Singleton for enforcing just one HTML Purifier in your system

```php
public static getInstance(\HTMLPurifier|\HTMLPurifier_Config $prototype = null): \HTMLPurifier
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prototype` | **\HTMLPurifier&#124;\HTMLPurifier_Config** | Optional prototype<br />HTMLPurifier instance to overload singleton with,<br />or HTMLPurifier_Config instance to configure the<br />generated version with. |





***


***
> Automatically generated on 2025-03-18
