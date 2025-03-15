
# HTMLPurifier_HTMLDefinition

Definition of the purified HTML that describes allowed children,
attributes, and many other things.

Conventions:

All member variables that are prefixed with info
(including the main $info array) are used by HTML Purifier internals
and should not be directly edited when customizing the HTMLDefinition.
They can usually be set via configuration directives or custom
modules.

On the other hand, member variables without the info prefix are used
internally by the HTMLDefinition and MUST NOT be used by other HTML
Purifier internals. Many of them, however, are public, and may be
edited by userspace code to tweak the behavior of HTMLDefinition.

* Full name: `\HTMLPurifier_HTMLDefinition`
* Parent class: [`\HTMLPurifier_Definition`](./HTMLPurifier_Definition.md)



## Properties


### info

Associative array of element names to HTMLPurifier_ElementDef.

```php
public $info
```






***

### info_global_attr

Associative array of global attribute name to attribute definition.

```php
public $info_global_attr
```






***

### info_parent

String name of parent element HTML will be going into.

```php
public $info_parent
```






***

### info_parent_def

Definition for parent element, allows parent element to be a
tag that's not allowed inside the HTML fragment.

```php
public $info_parent_def
```






***

### info_block_wrapper

String name of element used to wrap inline elements in block context.

```php
public $info_block_wrapper
```






***

### info_tag_transform

Associative array of deprecated tag name to HTMLPurifier_TagTransform.

```php
public $info_tag_transform
```






***

### info_attr_transform_pre

Indexed list of HTMLPurifier_AttrTransform to be performed before validation.

```php
public $info_attr_transform_pre
```






***

### info_attr_transform_post

Indexed list of HTMLPurifier_AttrTransform to be performed after validation.

```php
public $info_attr_transform_post
```






***

### info_content_sets

Nested lookup array of content set name (Block, Inline) to
element name to whether or not it belongs in that content set.

```php
public $info_content_sets
```






***

### info_injector

Indexed list of HTMLPurifier_Injector to be used.

```php
public $info_injector
```






***

### doctype

Doctype object

```php
public $doctype
```






***

### _anonModule



```php
private $_anonModule
```






***

### type

What type of definition is it?

```php
public $type
```






***

### manager



```php
public $manager
```






***

## Methods


### addAttribute

Adds a custom attribute to a pre-existing element

```php
public addAttribute(string $element_name, string $attr_name, mixed $def): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element_name` | **string** | Element name to add attribute to |
| `$attr_name` | **string** | Name of attribute |
| `$def` | **mixed** | Attribute definition, can be string or object, see<br />HTMLPurifier_AttrTypes for details |





***

### addElement

Adds a custom element to your HTML definition

```php
public addElement(mixed $element_name, mixed $type, mixed $contents, mixed $attr_collections, mixed $attributes = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element_name` | **mixed** |  |
| `$type` | **mixed** |  |
| `$contents` | **mixed** |  |
| `$attr_collections` | **mixed** |  |
| `$attributes` | **mixed** |  |





**See Also:**

* \HTMLPurifier_HTMLModule::addElement() - for detailed
parameter and return value descriptions.

***

### addBlankElement

Adds a blank element to your HTML definition, for overriding
existing behavior

```php
public addBlankElement(string $element_name): \HTMLPurifier_ElementDef
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element_name` | **string** |  |





**See Also:**

* \HTMLPurifier_HTMLModule::addBlankElement() - for detailed
parameter and return value descriptions.

***

### getAnonymousModule

Retrieves a reference to the anonymous module, so you can
bust out advanced features without having to make your own
module.

```php
public getAnonymousModule(): \HTMLPurifier_HTMLModule
```












***

### __construct

Performs low-cost, preliminary initialization.

```php
public __construct(): mixed
```












***

### doSetup

Sets up the definition object into the final form, something
not done by the constructor

```php
protected doSetup(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### processModules

Extract out the information from the manager

```php
protected processModules(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### setupConfigStuff

Sets up stuff based on config. We need a better way of doing this.

```php
protected setupConfigStuff(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### parseTinyMCEAllowedList

Parses a TinyMCE-flavored Allowed Elements and Attributes list into
separate lists for processing. Format is element[attr1|attr2],element2.

```php
public parseTinyMCEAllowedList(array $list): array
```

..






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$list` | **array** | String list to parse |





***


## Inherited methods


### doSetup

Sets up the definition object into the final form, something
not done by the constructor

```php
protected doSetup(\HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### setup

Setup function that aborts if already setup

```php
public setup(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***


***
> Automatically generated on 2025-03-15
