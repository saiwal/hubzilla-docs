***

# HTMLPurifier_AttrTransform_EnumToCSS

Generic pre-transform that converts an attribute with a fixed number of
values (enumerated) to CSS.



* Full name: `\HTMLPurifier_AttrTransform_EnumToCSS`
* Parent class: [`\HTMLPurifier_AttrTransform`](./HTMLPurifier_AttrTransform.md)



## Properties


### attr

Name of attribute to transform from.

```php
protected $attr
```






***

### enumToCSS

Lookup array of attribute values to CSS.

```php
protected $enumToCSS
```






***

### caseSensitive

Case sensitivity of the matching.

```php
protected $caseSensitive
```






***

## Methods


### __construct



```php
public __construct(string $attr, array $enum_to_css, bool $case_sensitive = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attr` | **string** | Attribute name to transform from |
| `$enum_to_css` | **array** | Lookup array of attribute values to CSS |
| `$case_sensitive` | **bool** | Case sensitivity indicator, default false |





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
> Automatically generated on 2025-03-15
