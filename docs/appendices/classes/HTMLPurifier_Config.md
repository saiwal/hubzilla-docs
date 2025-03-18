
# HTMLPurifier_Config

Configuration object that triggers customizable behavior.



* Full name: `\HTMLPurifier_Config`



## Properties


### version

HTML Purifier's version

```php
public $version
```






***

### autoFinalize

Whether or not to automatically finalize
the object if a read operation is done.

```php
public $autoFinalize
```






***

### serials

Namespace indexed array of serials for specific namespaces.

```php
protected $serials
```





**See Also:**

* \getSerial() - for more info.

***

### serial

Serial for entire configuration object.

```php
protected $serial
```






***

### parser

Parser for variables.

```php
protected $parser
```






***

### def

Reference HTMLPurifier_ConfigSchema for value checking.

```php
public $def
```






***

### definitions

Indexed array of definitions.

```php
protected $definitions
```






***

### finalized

Whether or not config is finalized.

```php
protected $finalized
```






***

### plist

Property list containing configuration directives.

```php
protected $plist
```






***

### aliasMode

Whether or not a set is taking place due to an alias lookup.

```php
private $aliasMode
```






***

### chatty

Set to false if you do not want line and file numbers in errors.

```php
public $chatty
```

(useful when unit testing).  This will also compress some errors
and exceptions.




***

### lock

Current lock; only gets to this namespace are allowed.

```php
private $lock
```






***

## Methods


### __construct

Constructor

```php
public __construct(\HTMLPurifier_ConfigSchema $definition, \HTMLPurifier_PropertyList $parent = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$definition` | **\HTMLPurifier_ConfigSchema** | ConfigSchema that defines<br />what directives are allowed. |
| `$parent` | **\HTMLPurifier_PropertyList** |  |





***

### create

Convenience constructor that creates a config object based on a mixed var

```php
public static create(mixed $config, \HTMLPurifier_ConfigSchema $schema = null): \HTMLPurifier_Config
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **mixed** | Variable that defines the state of the config<br />object. Can be: a HTMLPurifier_Config() object,<br />an array of directives based on loadArray(),<br />or a string filename of an ini file. |
| `$schema` | **\HTMLPurifier_ConfigSchema** | Schema object |


**Return Value:**

Configured object




***

### inherit

Creates a new config object that inherits from a previous one.

```php
public static inherit(\HTMLPurifier_Config $config): \HTMLPurifier_Config
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** | Configuration object to inherit from. |


**Return Value:**

object with $config as its parent.




***

### createDefault

Convenience constructor that creates a default configuration object.

```php
public static createDefault(): \HTMLPurifier_Config
```



* This method is **static**.





**Return Value:**

default object.




***

### get

Retrieves a value from the configuration.

```php
public get(string $key, mixed $a = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** | String key |
| `$a` | **mixed** |  |





***

### getBatch

Retrieves an array of directives to values from a given namespace

```php
public getBatch(string $namespace): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$namespace` | **string** | String namespace |





***

### getBatchSerial

Returns a SHA-1 signature of a segment of the configuration object
that uniquely identifies that particular configuration

```php
public getBatchSerial(string $namespace): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$namespace` | **string** | Namespace to get serial for |





***

### getSerial

Returns a SHA-1 signature for the entire configuration object
that uniquely identifies that particular configuration

```php
public getSerial(): string
```












***

### getAll

Retrieves all directives, organized by namespace

```php
public getAll(): mixed
```












***

### set

Sets a value to configuration.

```php
public set(string $key, mixed $value, mixed $a = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** | key |
| `$value` | **mixed** | value |
| `$a` | **mixed** |  |





***

### _listify

Convenience function for error reporting

```php
private _listify(array $lookup): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lookup` | **array** |  |





***

### getHTMLDefinition

Retrieves object reference to the HTML definition.

```php
public getHTMLDefinition(bool $raw = false, bool $optimized = false): \HTMLPurifier_HTMLDefinition|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$raw` | **bool** | Return a copy that has not been setup yet. Must be<br />called before it&#039;s been setup, otherwise won&#039;t work. |
| `$optimized` | **bool** | If true, this method may return null, to<br />indicate that a cached version of the modified<br />definition object is available and no further edits<br />are necessary.  Consider using<br />maybeGetRawHTMLDefinition, which is more explicitly<br />named, instead. |





***

### getCSSDefinition

Retrieves object reference to the CSS definition

```php
public getCSSDefinition(bool $raw = false, bool $optimized = false): \HTMLPurifier_CSSDefinition|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$raw` | **bool** | Return a copy that has not been setup yet. Must be<br />called before it&#039;s been setup, otherwise won&#039;t work. |
| `$optimized` | **bool** | If true, this method may return null, to<br />indicate that a cached version of the modified<br />definition object is available and no further edits<br />are necessary.  Consider using<br />maybeGetRawCSSDefinition, which is more explicitly<br />named, instead. |





***

### getURIDefinition

Retrieves object reference to the URI definition

```php
public getURIDefinition(bool $raw = false, bool $optimized = false): \HTMLPurifier_URIDefinition|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$raw` | **bool** | Return a copy that has not been setup yet. Must be<br />called before it&#039;s been setup, otherwise won&#039;t work. |
| `$optimized` | **bool** | If true, this method may return null, to<br />indicate that a cached version of the modified<br />definition object is available and no further edits<br />are necessary.  Consider using<br />maybeGetRawURIDefinition, which is more explicitly<br />named, instead. |





***

### getDefinition

Retrieves a definition

```php
public getDefinition(string $type, bool $raw = false, bool $optimized = false): \HTMLPurifier_Definition|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | Type of definition: HTML, CSS, etc |
| `$raw` | **bool** | Whether or not definition should be returned raw |
| `$optimized` | **bool** | Only has an effect when $raw is true.  Whether<br />or not to return null if the result is already present in<br />the cache.  This is off by default for backwards<br />compatibility reasons, but you need to do things this<br />way in order to ensure that caching is done properly.<br />Check out enduser-customize.html for more details.<br />We probably won&#039;t ever change this default, as much as the<br />maybe semantics is the &quot;right thing to do.&quot; |




**Throws:**

- [`HTMLPurifier_Exception`](./HTMLPurifier_Exception.md)



***

### initDefinition

Initialise definition

```php
private initDefinition(string $type): \HTMLPurifier_CSSDefinition|\HTMLPurifier_HTMLDefinition|\HTMLPurifier_URIDefinition
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | What type of definition to create |




**Throws:**

- [`HTMLPurifier_Exception`](./HTMLPurifier_Exception.md)



***

### maybeGetRawDefinition



```php
public maybeGetRawDefinition(mixed $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |





***

### maybeGetRawHTMLDefinition



```php
public maybeGetRawHTMLDefinition(): \HTMLPurifier_HTMLDefinition|null
```












***

### maybeGetRawCSSDefinition



```php
public maybeGetRawCSSDefinition(): \HTMLPurifier_CSSDefinition|null
```












***

### maybeGetRawURIDefinition



```php
public maybeGetRawURIDefinition(): \HTMLPurifier_URIDefinition|null
```












***

### loadArray

Loads configuration values from an array with the following structure:
Namespace.Directive => Value

```php
public loadArray(array $config_array): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config_array` | **array** | Configuration associative array |





***

### getAllowedDirectivesForForm

Returns a list of array(namespace, directive) for all directives
that are allowed in a web-form context as per an allowed
namespaces/directives list.

```php
public static getAllowedDirectivesForForm(array $allowed, \HTMLPurifier_ConfigSchema $schema = null): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$allowed` | **array** | List of allowed namespaces/directives |
| `$schema` | **\HTMLPurifier_ConfigSchema** | Schema to use, if not global copy |





***

### loadArrayFromForm

Loads configuration values from $_GET/$_POST that were posted
via ConfigForm

```php
public static loadArrayFromForm(array $array, string|bool $index = false, array|bool $allowed = true, bool $mq_fix = true, \HTMLPurifier_ConfigSchema $schema = null): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array` | **array** | $_GET or $_POST array to import |
| `$index` | **string&#124;bool** | Index/name that the config variables are in |
| `$allowed` | **array&#124;bool** | List of allowed namespaces/directives |
| `$mq_fix` | **bool** | Boolean whether or not to enable magic quotes fix |
| `$schema` | **\HTMLPurifier_ConfigSchema** | Schema to use, if not global copy |





***

### mergeArrayFromForm

Merges in configuration values from $_GET/$_POST to object. NOT STATIC.

```php
public mergeArrayFromForm(array $array, string|bool $index = false, array|bool $allowed = true, bool $mq_fix = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array` | **array** | $_GET or $_POST array to import |
| `$index` | **string&#124;bool** | Index/name that the config variables are in |
| `$allowed` | **array&#124;bool** | List of allowed namespaces/directives |
| `$mq_fix` | **bool** | Boolean whether or not to enable magic quotes fix |





***

### prepareArrayFromForm

Prepares an array from a form into something usable for the more
strict parts of HTMLPurifier_Config

```php
public static prepareArrayFromForm(array $array, string|bool $index = false, array|bool $allowed = true, bool $mq_fix = true, \HTMLPurifier_ConfigSchema $schema = null): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array` | **array** | $_GET or $_POST array to import |
| `$index` | **string&#124;bool** | Index/name that the config variables are in |
| `$allowed` | **array&#124;bool** | List of allowed namespaces/directives |
| `$mq_fix` | **bool** | Boolean whether or not to enable magic quotes fix |
| `$schema` | **\HTMLPurifier_ConfigSchema** | Schema to use, if not global copy |





***

### loadIni

Loads configuration values from an ini file

```php
public loadIni(string $filename): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** | Name of ini file |





***

### isFinalized

Checks whether or not the configuration object is finalized.

```php
public isFinalized(string|bool $error = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$error` | **string&#124;bool** | String error message, or false for no error |





***

### autoFinalize

Finalizes configuration only if auto finalize is on and not
already finalized

```php
public autoFinalize(): mixed
```












***

### finalize

Finalizes a configuration object, prohibiting further change

```php
public finalize(): mixed
```












***

### triggerError

Produces a nicely formatted error message by supplying the
stack frame information OUTSIDE of HTMLPurifier_Config.

```php
protected triggerError(string $msg, int $no): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$msg` | **string** | An error message |
| `$no` | **int** | An error number |





***

### serialize

Returns a serialized form of the configuration object that can
be reconstituted.

```php
public serialize(): string
```












***


***
> Automatically generated on 2025-03-18
