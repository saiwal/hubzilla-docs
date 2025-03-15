***

# HTMLPurifier_HTMLModuleManager





* Full name: `\HTMLPurifier_HTMLModuleManager`



## Properties


### doctypes



```php
public $doctypes
```






***

### doctype

Instance of current doctype.

```php
public $doctype
```






***

### attrTypes



```php
public $attrTypes
```






***

### modules

Active instances of modules for the specified doctype are
indexed, by name, in this array.

```php
public $modules
```






***

### registeredModules

Array of recognized HTMLPurifier_HTMLModule instances,
indexed by module's class name. This array is usually lazy loaded, but a
user can overload a module by pre-emptively registering it.

```php
public $registeredModules
```






***

### userModules

List of extra modules that were added by the user
using addModule(). These get unconditionally merged into the current doctype, whatever
it may be.

```php
public $userModules
```






***

### elementLookup

Associative array of element name to list of modules that have
definitions for the element; this array is dynamically filled.

```php
public $elementLookup
```






***

### prefixes

List of prefixes we should use for registering small names.

```php
public $prefixes
```






***

### contentSets



```php
public $contentSets
```






***

### attrCollections



```php
public $attrCollections
```






***

### trusted

If set to true, unsafe elements and attributes will be allowed.

```php
public $trusted
```






***

## Methods


### __construct



```php
public __construct(): mixed
```












***

### registerModule

Registers a module to the recognized module list, useful for
overloading pre-existing modules.

```php
public registerModule(mixed $module, mixed $overload = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$module` | **mixed** | Mixed: string module name, with or without<br />HTMLPurifier_HTMLModule prefix, or instance of<br />subclass of HTMLPurifier_HTMLModule. |
| `$overload` | **mixed** | Boolean whether or not to overload previous modules.<br />If this is not set, and you do overload a module,<br />HTML Purifier will complain with a warning. |





***

### addModule

Adds a module to the current doctype by first registering it,
and then tacking it on to the active doctype

```php
public addModule(mixed $module): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$module` | **mixed** |  |





***

### addPrefix

Adds a class prefix that registerModule() will use to resolve a
string name to a concrete class

```php
public addPrefix(mixed $prefix): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prefix` | **mixed** |  |





***

### setup

Performs processing on modules, after being called you may
use getElement() and getElements()

```php
public setup(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### processModule

Takes a module and adds it to the active module collection,
registering it if necessary.

```php
public processModule(mixed $module): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$module` | **mixed** |  |





***

### getElements

Retrieves merged element definitions.

```php
public getElements(): array
```









**Return Value:**

of HTMLPurifier_ElementDef




***

### getElement

Retrieves a single merged element definition

```php
public getElement(string $name, bool $trusted = null): \HTMLPurifier_ElementDef
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Name of element |
| `$trusted` | **bool** | Boolean trusted overriding parameter: set to true<br />if you want the full version of an element |


**Return Value:**

Merged HTMLPurifier_ElementDef




***


***
> Automatically generated on 2025-03-15
