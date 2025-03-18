
# HTMLPurifier_AttrTransform_Length

Class for handling width/height length attribute transformations to CSS



* Full name: `\HTMLPurifier_AttrTransform_Length`
* Parent class: [`\HTMLPurifier_AttrTransform`](./HTMLPurifier_AttrTransform.md)



## Properties


### name



```php
protected $name
```






***

### cssName



```php
protected $cssName
```






***

## Methods


### __construct



```php
public __construct(mixed $name, mixed $css_name = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |
| `$css_name` | **mixed** |  |





***

### transform

Abstract: makes changes to the attributes dependent on multiple values.

```php
public transform(array $attr, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attr` | **array** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***


## Inherited methods


### transform

Abstract: makes changes to the attributes dependent on multiple values.

```php
public transform(array $attr, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): array
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attr` | **array** | Assoc array of attributes, usually from<br />HTMLPurifier_Token_Tag::$attr |
| `$config` | **\HTMLPurifier_Config** | Mandatory HTMLPurifier_Config object. |
| `$context` | **\HTMLPurifier_Context** | Mandatory HTMLPurifier_Context object |


**Return Value:**

Processed attribute array.




***

### prependCSS

Prepends CSS properties to the style attribute, creating the
attribute if it doesn't exist.

```php
public prependCSS(array& $attr, string $css): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attr` | **array** | Attribute array to process (passed by reference) |
| `$css` | **string** | CSS to prepend |





***

### confiscateAttr

Retrieves and removes an attribute

```php
public confiscateAttr(array& $attr, mixed $key): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attr` | **array** | Attribute array to process (passed by reference) |
| `$key` | **mixed** | Key of attribute to confiscate |





***


***
> Automatically generated on 2025-03-18
