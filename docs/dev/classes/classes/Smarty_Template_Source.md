
# Smarty_Template_Source

Smarty Resource Data Object
Meta Data Container for Template Files



* Full name: `\Smarty_Template_Source`



## Properties


### uid

Unique Template ID

```php
public string $uid
```






***

### resource

Template Resource (Smarty_Internal_Template::$template_resource)

```php
public string $resource
```






***

### type

Resource Type

```php
public string $type
```






***

### name

Resource Name

```php
public string $name
```






***

### filepath

Source Filepath

```php
public string $filepath
```






***

### timestamp

Source Timestamp

```php
public int $timestamp
```






***

### exists

Source Existence

```php
public bool $exists
```






***

### basename

Source File Base name

```php
public string $basename
```






***

### components

The Components an extended template is made of

```php
public \Smarty_Template_Source[] $components
```






***

### handler

Resource Handler

```php
public \Smarty_Resource $handler
```






***

### smarty

Smarty instance

```php
public \Smarty $smarty
```






***

### isConfig

Resource is source

```php
public bool $isConfig
```






***

### content

Template source content eventually set by default handler

```php
public string $content
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
