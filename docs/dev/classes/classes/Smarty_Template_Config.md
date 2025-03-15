***

# Smarty_Template_Config

Smarty Config Resource Data Object
Meta Data Container for Template Files



* Full name: `\Smarty_Template_Config`
* Parent class: [`\Smarty_Template_Source`](./Smarty_Template_Source.md)



## Properties


### config_sections

array of section names, single section or null

```php
public null|string|array $config_sections
```






***

### scope

scope into which the config variables shall be loaded

```php
public int $scope
```






***

### isConfig

Flag that source is a config file

```php
public bool $isConfig
```






***

### compiler_class

Name of the Class to compile this resource's contents with

```php
public string $compiler_class
```






***

### template_lexer_class

Name of the Class to tokenize this resource's contents with

```php
public string $template_lexer_class
```






***

### template_parser_class

Name of the Class to parse this resource's contents with

```php
public string $template_parser_class
```






***

## Methods


### load

initialize Source Object for given resource
Either [$_template] or [$smarty, $template_resource] must be specified

```php
public static load(\Smarty_Internal_Template $_template = null, \Smarty $smarty = null, string $template_resource = null): \Smarty_Template_Config
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |
| `$smarty` | **\Smarty** | smarty object |
| `$template_resource` | **string** | resource identifier |


**Return Value:**

Source Object



**Throws:**

- [`SmartyException`](./SmartyException.md)



***


## Inherited methods


### load

initialize Source Object for given resource
Either [$_template] or [$smarty, $template_resource] must be specified

```php
public static load(\Smarty_Internal_Template $_template = null, \Smarty $smarty = null, string $template_resource = null): \Smarty_Template_Source
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$_template` | **\Smarty_Internal_Template** | template object |
| `$smarty` | **\Smarty** | smarty object |
| `$template_resource` | **string** | resource identifier |


**Return Value:**

Source Object



**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### getTimeStamp

Get source time stamp

```php
public getTimeStamp(): int
```












***

### getContent

Get source content

```php
public getContent(): string
```











**Throws:**

- [`SmartyException`](./SmartyException.md)



***


***
> Automatically generated on 2025-03-15
