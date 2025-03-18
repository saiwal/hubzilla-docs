
# HTMLPurifier_TagTransform_Simple

Simple transformation, just change tag name to something else,
and possibly add some styling. This will cover most of the deprecated
tag cases.



* Full name: `\HTMLPurifier_TagTransform_Simple`
* Parent class: [`\HTMLPurifier_TagTransform`](./HTMLPurifier_TagTransform.md)



## Properties


### style



```php
protected $style
```






***

## Methods


### __construct



```php
public __construct(string $transform_to, string $style = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$transform_to` | **string** | Tag name to transform to. |
| `$style` | **string** | CSS style to add to the tag |





***

### transform

Transforms the obsolete tag into the valid tag.

```php
public transform(\HTMLPurifier_Token_Tag $tag, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **\HTMLPurifier_Token_Tag** |  |
| `$config` | **\HTMLPurifier_Config** |  |
| `$context` | **\HTMLPurifier_Context** |  |





***


## Inherited methods


### transform

Transforms the obsolete tag into the valid tag.

```php
public transform(\HTMLPurifier_Token_Tag $tag, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **\HTMLPurifier_Token_Tag** | Tag to be transformed. |
| `$config` | **\HTMLPurifier_Config** | Mandatory HTMLPurifier_Config object |
| `$context` | **\HTMLPurifier_Context** | Mandatory HTMLPurifier_Context object |





***

### prependCSS

Prepends CSS properties to the style attribute, creating the
attribute if it doesn't exist.

```php
protected prependCSS(array& $attr, string $css): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attr` | **array** | Attribute array to process (passed by reference) |
| `$css` | **string** | CSS to prepend |





***


***
> Automatically generated on 2025-03-18
