***

# Smarty_Security

This class does contain the security settings



* Full name: `\Smarty_Security`



## Properties


### secure_dir

This is the list of template directories that are considered secure.

```php
public array $secure_dir
```

$template_dir is in this list implicitly.




***

### trusted_dir

This is an array of directories where trusted php scripts reside.

```php
public array $trusted_dir
```

{@link $security} is disabled during their inclusion/execution.




***

### trusted_uri

List of regular expressions (PCRE) that include trusted URIs

```php
public array $trusted_uri
```






***

### trusted_constants

List of trusted constants names

```php
public array $trusted_constants
```






***

### static_classes

This is an array of trusted static classes.

```php
public array $static_classes
```

If empty access to all static classes is allowed.
If set to 'none' none is allowed.




***

### trusted_static_methods

This is an nested array of trusted classes and static methods.

```php
public array $trusted_static_methods
```

If empty access to all static classes and methods is allowed.
Format:
array (
        'class_1' => array('method_1', 'method_2'), // allowed methods listed
        'class_2' => array(),                       // all methods of class allowed
      )
If set to null none is allowed.




***

### trusted_static_properties

This is an array of trusted static properties.

```php
public array $trusted_static_properties
```

If empty access to all static classes and properties is allowed.
Format:
array (
        'class_1' => array('prop_1', 'prop_2'), // allowed properties listed
        'class_2' => array(),                   // all properties of class allowed
      )
If set to null none is allowed.




***

### php_functions

This is an array of trusted PHP functions.

```php
public array $php_functions
```

If empty all functions are allowed.
To disable all PHP functions set $php_functions = null.




***

### php_modifiers

This is an array of trusted PHP modifiers.

```php
public array $php_modifiers
```

If empty all modifiers are allowed.
To disable all modifier set $php_modifiers = null.




***

### allowed_tags

This is an array of allowed tags.

```php
public array $allowed_tags
```

If empty no restriction by allowed_tags.




***

### disabled_tags

This is an array of disabled tags.

```php
public array $disabled_tags
```

If empty no restriction by disabled_tags.




***

### allowed_modifiers

This is an array of allowed modifier plugins.

```php
public array $allowed_modifiers
```

If empty no restriction by allowed_modifiers.




***

### disabled_modifiers

This is an array of disabled modifier plugins.

```php
public array $disabled_modifiers
```

If empty no restriction by disabled_modifiers.




***

### disabled_special_smarty_vars

This is an array of disabled special $smarty variables.

```php
public array $disabled_special_smarty_vars
```






***

### streams

This is an array of trusted streams.

```php
public array $streams
```

If empty all streams are allowed.
To disable all streams set $streams = null.




***

### allow_constants

+ flag if constants can be accessed from template

```php
public bool $allow_constants
```






***

### allow_super_globals

+ flag if super globals can be accessed from template

```php
public bool $allow_super_globals
```






***

### max_template_nesting

max template nesting level

```php
public int $max_template_nesting
```






***

### _current_template_nesting

current template nesting level

```php
private int $_current_template_nesting
```






***

### _resource_dir

Cache for $resource_dir lookup

```php
protected array $_resource_dir
```






***

### _template_dir

Cache for $template_dir lookup

```php
protected array $_template_dir
```






***

### _config_dir

Cache for $config_dir lookup

```php
protected array $_config_dir
```






***

### _secure_dir

Cache for $secure_dir lookup

```php
protected array $_secure_dir
```






***

### _php_resource_dir

Cache for $php_resource_dir lookup

```php
protected array $_php_resource_dir
```






***

### _trusted_dir

Cache for $trusted_dir lookup

```php
protected array $_trusted_dir
```






***

### _include_path_status

Cache for include path status

```php
protected bool $_include_path_status
```






***

### _include_dir

Cache for $_include_array lookup

```php
protected array $_include_dir
```






***

## Methods


### __construct



```php
public __construct(\Smarty $smarty): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |





***

### isTrustedPhpFunction

Check if PHP function is trusted.

```php
public isTrustedPhpFunction(string $function_name, object $compiler): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$function_name` | **string** |  |
| `$compiler` | **object** | compiler object |


**Return Value:**

true if function is trusted




***

### isTrustedStaticClass

Check if static class is trusted.

```php
public isTrustedStaticClass(string $class_name, object $compiler): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class_name` | **string** |  |
| `$compiler` | **object** | compiler object |


**Return Value:**

true if class is trusted




***

### isTrustedStaticClassAccess

Check if static class method/property is trusted.

```php
public isTrustedStaticClassAccess(string $class_name, string $params, object $compiler): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class_name` | **string** |  |
| `$params` | **string** |  |
| `$compiler` | **object** | compiler object |


**Return Value:**

true if class method is trusted




***

### isTrustedPhpModifier

Check if PHP modifier is trusted.

```php
public isTrustedPhpModifier(string $modifier_name, object $compiler): bool
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$modifier_name` | **string** |  |
| `$compiler` | **object** | compiler object |


**Return Value:**

true if modifier is trusted




***

### isTrustedTag

Check if tag is trusted.

```php
public isTrustedTag(string $tag_name, object $compiler): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag_name` | **string** |  |
| `$compiler` | **object** | compiler object |


**Return Value:**

true if tag is trusted




***

### isTrustedSpecialSmartyVar

Check if special $smarty variable is trusted.

```php
public isTrustedSpecialSmartyVar(string $var_name, object $compiler): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$var_name` | **string** |  |
| `$compiler` | **object** | compiler object |


**Return Value:**

true if tag is trusted




***

### isTrustedModifier

Check if modifier plugin is trusted.

```php
public isTrustedModifier(string $modifier_name, object $compiler): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$modifier_name` | **string** |  |
| `$compiler` | **object** | compiler object |


**Return Value:**

true if tag is trusted




***

### isTrustedConstant

Check if constants are enabled or trusted

```php
public isTrustedConstant(string $const, object $compiler): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$const` | **string** | constant name |
| `$compiler` | **object** | compiler object |





***

### isTrustedStream

Check if stream is trusted.

```php
public isTrustedStream(string $stream_name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stream_name` | **string** |  |


**Return Value:**

true if stream is trusted



**Throws:**
<p>if stream is not trusted</p>

- [`SmartyException`](./SmartyException.md)



***

### isTrustedResourceDir

Check if directory of file resource is trusted.

```php
public isTrustedResourceDir(string $filepath, null|bool $isConfig = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filepath` | **string** |  |
| `$isConfig` | **null&#124;bool** |  |


**Return Value:**

true if directory is trusted



**Throws:**
<p>if directory is not trusted</p>

- [`SmartyException`](./SmartyException.md)



***

### isTrustedUri

Check if URI (e.g. {fetch} or {html_image}) is trusted
To simplify things, isTrustedUri() resolves all input to "{$PROTOCOL}://{$HOSTNAME}".

```php
public isTrustedUri(string $uri): bool
```

So "http://username:password@hello.world.example.org:8080/some-path?some=query-string"
is reduced to "http://hello.world.example.org" prior to applying the patters from {@link $trusted_uri}.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |


**Return Value:**

true if URI is trusted



**Throws:**
<p>if URI is not trusted</p>

- [`SmartyException`](./SmartyException.md)



***

### _updateResourceDir

Remove old directories and its sub folders, add new directories

```php
private _updateResourceDir(array $oldDir, array $newDir): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$oldDir` | **array** |  |
| `$newDir` | **array** |  |





***

### _checkDir

Check if file is inside a valid directory

```php
private _checkDir(string $filepath, array $dirs): array|bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filepath` | **string** |  |
| `$dirs` | **array** | valid directories |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### enableSecurity

Loads security class and enables security

```php
public static enableSecurity(\Smarty $smarty, string|\Smarty_Security $security_class): \Smarty
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |
| `$security_class` | **string&#124;\Smarty_Security** | if a string is used, it must be class-name |


**Return Value:**

current Smarty instance for chaining



**Throws:**
<p>when an invalid class name is provided</p>

- [`SmartyException`](./SmartyException.md)



***

### startTemplate

Start template processing

```php
public startTemplate(mixed $template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **mixed** |  |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***

### endTemplate

Exit template processing

```php
public endTemplate(): mixed
```












***

### registerCallBacks

Register callback functions call at start/end of template rendering

```php
public registerCallBacks(\Smarty_Internal_Template $template): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **\Smarty_Internal_Template** |  |





***


***
> Automatically generated on 2025-03-15
