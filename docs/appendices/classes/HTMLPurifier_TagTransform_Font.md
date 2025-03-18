
# HTMLPurifier_TagTransform_Font

Transforms FONT tags to the proper form (SPAN with CSS styling)

This transformation takes the three proprietary attributes of FONT and
transforms them into their corresponding CSS attributes.  These are color,
face, and size.

* Full name: `\HTMLPurifier_TagTransform_Font`
* Parent class: [`\HTMLPurifier_TagTransform`](./HTMLPurifier_TagTransform.md)



## Properties


### transform_to

Tag name to transform the tag to.

```php
public $transform_to
```






***

### _size_lookup



```php
protected $_size_lookup
```






***

## Methods


### transform

Transforms the obsolete tag into the valid tag.

```php
public transform(\HTMLPurifier_Token_Tag $tag, \HTMLPurifier_Config $config, \HTMLPurifier_Context $context): \HTMLPurifier_Token_End|string
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
