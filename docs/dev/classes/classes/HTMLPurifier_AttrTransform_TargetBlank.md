
# HTMLPurifier_AttrTransform_TargetBlank

Adds target="blank" to all outbound links.  This transform is
only attached if Attr.TargetBlank is TRUE.  This works regardless
of whether or not Attr.AllowedFrameTargets



* Full name: `\HTMLPurifier_AttrTransform_TargetBlank`
* Parent class: [`\HTMLPurifier_AttrTransform`](./HTMLPurifier_AttrTransform.md)



## Properties


### parser



```php
private $parser
```






***

## Methods


### __construct



```php
public __construct(): mixed
```












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
