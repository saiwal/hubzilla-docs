
# Smarty_Internal_Resource_File

Smarty Internal Plugin Resource File
Implements the file system as resource for Smarty templates



* Full name: `\Smarty_Internal_Resource_File`
* Parent class: [`\Smarty_Resource`](./Smarty_Resource.md)




## Methods


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




**Throws:**

- [`SmartyException`](./SmartyException.md)



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

### getContent

Load template's source from file into current template object

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

### buildFilepath

build template filepath by traversing the template_dir array

```php
protected buildFilepath(\Smarty_Template_Source $source, \Smarty_Internal_Template $_template = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **\Smarty_Template_Source** | source object |
| `$_template` | **\Smarty_Internal_Template** | template object |


**Return Value:**

fully qualified filepath



**Throws:**

- [`SmartyException`](./SmartyException.md)



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




* This method is **abstract**.



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




* This method is **abstract**.



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


***
> Automatically generated on 2025-03-15
