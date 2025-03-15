
# Smarty_Resource_Mysql

MySQL Resource
Resource Implementation based on the Custom API to use
MySQL as the storage resource for Smarty's templates and configs.

Table definition:
<pre>CREATE TABLE IF NOT EXISTS `templates` (
  `name` varchar(100) NOT NULL,
  `modified` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `source` text,
  PRIMARY KEY (`name`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;</pre>
Demo data:
<pre>INSERT INTO `templates` (`name`, `modified`, `source`) VALUES ('test.tpl', "2010-12-25 22:00:00", '{$x="hello
world"}{$x}');</pre>

* Full name: `\Smarty_Resource_Mysql`
* Parent class: [`\Smarty_Resource_Custom`](./Smarty_Resource_Custom.md)



## Properties


### db

PDO instance

```php
protected \PDO $db
```






***

### fetch

prepared fetch() statement

```php
protected \PDOStatement $fetch
```






***

### mtime

prepared fetchTimestamp() statement

```php
protected \PDOStatement $mtime
```






***

## Methods


### __construct

Smarty_Resource_Mysql constructor.

```php
public __construct(): mixed
```











**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### fetch

Fetch a template and its modification time from database

```php
protected fetch(string $name, string& $source, int& $mtime): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | template name |
| `$source` | **string** | template source |
| `$mtime` | **int** | template modification timestamp (epoch) |





***

### fetchTimestamp

Fetch a template's modification time from database

```php
protected fetchTimestamp(string $name): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | template name |


**Return Value:**

timestamp (epoch) the template was modified




***


## Inherited methods


### load

Load Resource Handler

```php
public static load(\Smarty $smarty, string $type): \Smarty_Resource
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** | smarty object |
| `$type` | **string** | name of the resource |


**Return Value:**

Resource Handler



**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### parseResourceName

extract resource_type and resource_name from template_resource and config_resource

```php
public static parseResourceName(string $resource_name, string $default_resource): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$resource_name` | **string** | template_resource or config_resource to parse |
| `$default_resource` | **string** | the default resource_type defined in $smarty |


**Return Value:**

with parsed resource name and type




***

### getUniqueTemplateName

modify template_resource according to resource handlers specifications

```php
public static getUniqueTemplateName(\Smarty_Internal_Template|\Smarty $obj, string $template_resource): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **\Smarty_Internal_Template&#124;\Smarty** | Smarty instance |
| `$template_resource` | **string** | template_resource to extract resource handler and<br />name of |


**Return Value:**

unique resource name



**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### source

initialize Source Object for given resource
wrapper for backward compatibility to versions < 3.1.22
Either [$_template] or [$smarty, $template_resource] must be specified

```php
public static source(\Smarty_Internal_Template $_template = null, \Smarty $smarty = null, string $template_resource = null): \Smarty_Template_Source
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

### getContent

Load template's source into current template object

```php
public getContent(\Smarty_Template_Source $source): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **\Smarty_Template_Source** | source object |


**Return Value:**

template source



**Throws:**
<p>if source cannot be loaded</p>

- [`SmartyException`](./SmartyException.md)



***

### populate

populate Source Object with meta data from Resource

```php
public populate(\Smarty_Template_Source $source, \Smarty_Internal_Template $_template = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **\Smarty_Template_Source** | source object |
| `$_template` | **\Smarty_Internal_Template** | template object |





***

### populateTimestamp

populate Source Object with timestamp and exists from Resource

```php
public populateTimestamp(\Smarty_Template_Source $source): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **\Smarty_Template_Source** | source object |





***

### buildUniqueResourceName

modify resource_name according to resource handlers specifications

```php
public buildUniqueResourceName(\Smarty $smarty, string $resource_name, bool $isConfig = false): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** | Smarty instance |
| `$resource_name` | **string** | resource_name to make unique |
| `$isConfig` | **bool** | flag for config resource |


**Return Value:**

unique resource name




***

### getBasename

Determine basename for compiled filename

```php
public getBasename(\Smarty_Template_Source $source): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **\Smarty_Template_Source** | source object |


**Return Value:**

resource's basename




***

### checkTimestamps



```php
public checkTimestamps(): bool
```












***

### fetch

fetch template and its modification time from data source

```php
protected fetch(string $name, string& $source, int& $mtime): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | template name |
| `$source` | **string** | template source |
| `$mtime` | **int** | template modification timestamp (epoch) |





***

### fetchTimestamp

Fetch template's modification timestamp from data source
{@internal implementing this method is optional.

```php
protected fetchTimestamp(string $name): int|bool
```

Only implement it if modification times can be accessed faster than loading the complete template source.}}






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | template name |


**Return Value:**

timestamp (epoch) the template was modified, or false if not found




***

### generateSafeName

Removes special characters from $name and limits its length to 127 characters.

```php
private generateSafeName(mixed $name): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
