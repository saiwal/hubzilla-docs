***

# ClassLoader

ClassLoader implements a PSR-0, PSR-4 and classmap class loader.

$loader = new \Composer\Autoload\ClassLoader();

    // register classes with namespaces
    $loader->add('Symfony\Component', __DIR__.'/component');
    $loader->add('Symfony',           __DIR__.'/framework');

    // activate the autoloader
    $loader->register();

    // to enable searching the include path (eg. for PEAR packages)
    $loader->setUseIncludePath(true);

In this example, if you try to use a class in the Symfony\Component
namespace or one of its children (Symfony\Component\Console for instance),
the autoloader will first look for the class under the component/
directory, and it will then fallback to the framework/ directory if not
found before giving up.

This class is loosely based on the Symfony UniversalClassLoader.

* Full name: `\Composer\Autoload\ClassLoader`

**See Also:**

* https://www.php-fig.org/psr/psr-0/ - 
* https://www.php-fig.org/psr/psr-4/ - 



## Properties


### includeFile



```php
private static callable $includeFile
```



* This property is **static**.


***

### vendorDir



```php
private string|null $vendorDir
```






***

### prefixLengthsPsr4



```php
private array&lt;string,array&lt;string,int&gt;&gt; $prefixLengthsPsr4
```






***

### prefixDirsPsr4



```php
private array&lt;string,list&lt;string&gt;&gt; $prefixDirsPsr4
```






***

### fallbackDirsPsr4



```php
private list&lt;string&gt; $fallbackDirsPsr4
```






***

### prefixesPsr0

List of PSR-0 prefixes

```php
private array&lt;string,array&lt;string,list&lt;string&gt;&gt;&gt; $prefixesPsr0
```

Structured as array('F (first letter)' => array('Foo\Bar (full prefix)' => array('path', 'path2')))




***

### fallbackDirsPsr0



```php
private list&lt;string&gt; $fallbackDirsPsr0
```






***

### useIncludePath



```php
private bool $useIncludePath
```






***

### classMap



```php
private array&lt;string,string&gt; $classMap
```






***

### classMapAuthoritative



```php
private bool $classMapAuthoritative
```






***

### missingClasses



```php
private array&lt;string,bool&gt; $missingClasses
```






***

### apcuPrefix



```php
private string|null $apcuPrefix
```






***

### registeredLoaders



```php
private static array&lt;string,self&gt; $registeredLoaders
```



* This property is **static**.


***

## Methods


### __construct



```php
public __construct(string|null $vendorDir = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$vendorDir` | **string&#124;null** |  |





***

### getPrefixes



```php
public getPrefixes(): array&lt;string,list&lt;string&gt;&gt;
```












***

### getPrefixesPsr4



```php
public getPrefixesPsr4(): array&lt;string,list&lt;string&gt;&gt;
```












***

### getFallbackDirs



```php
public getFallbackDirs(): list&lt;string&gt;
```












***

### getFallbackDirsPsr4



```php
public getFallbackDirsPsr4(): list&lt;string&gt;
```












***

### getClassMap



```php
public getClassMap(): array&lt;string,string&gt;
```









**Return Value:**

Array of classname => path




***

### addClassMap



```php
public addClassMap(array&lt;string,string&gt; $classMap): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$classMap` | **array<string,string>** | Class to filename map |





***

### add

Registers a set of PSR-0 directories for a given prefix, either
appending or prepending to the ones previously set for this prefix.

```php
public add(string $prefix, list&lt;string&gt;|string $paths, bool $prepend = false): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prefix` | **string** | The prefix |
| `$paths` | **list<string>&#124;string** | The PSR-0 root directories |
| `$prepend` | **bool** | Whether to prepend the directories |





***

### addPsr4

Registers a set of PSR-4 directories for a given namespace, either
appending or prepending to the ones previously set for this namespace.

```php
public addPsr4(string $prefix, list&lt;string&gt;|string $paths, bool $prepend = false): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prefix` | **string** | The prefix/namespace, with trailing &#039;\\&#039; |
| `$paths` | **list<string>&#124;string** | The PSR-4 base directories |
| `$prepend` | **bool** | Whether to prepend the directories |




**Throws:**

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### set

Registers a set of PSR-0 directories for a given prefix,
replacing any others previously set for this prefix.

```php
public set(string $prefix, list&lt;string&gt;|string $paths): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prefix` | **string** | The prefix |
| `$paths` | **list<string>&#124;string** | The PSR-0 base directories |





***

### setPsr4

Registers a set of PSR-4 directories for a given namespace,
replacing any others previously set for this namespace.

```php
public setPsr4(string $prefix, list&lt;string&gt;|string $paths): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prefix` | **string** | The prefix/namespace, with trailing &#039;\\&#039; |
| `$paths` | **list<string>&#124;string** | The PSR-4 base directories |




**Throws:**

- [`InvalidArgumentException`](../../InvalidArgumentException.md)



***

### setUseIncludePath

Turns on searching the include path for class files.

```php
public setUseIncludePath(bool $useIncludePath): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$useIncludePath` | **bool** |  |





***

### getUseIncludePath

Can be used to check if the autoloader uses the include path to check
for classes.

```php
public getUseIncludePath(): bool
```












***

### setClassMapAuthoritative

Turns off searching the prefix and fallback directories for classes
that have not been registered with the class map.

```php
public setClassMapAuthoritative(bool $classMapAuthoritative): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$classMapAuthoritative` | **bool** |  |





***

### isClassMapAuthoritative

Should class lookup fail if not found in the current class map?

```php
public isClassMapAuthoritative(): bool
```












***

### setApcuPrefix

APCu prefix to use to cache found/not-found classes, if the extension is enabled.

```php
public setApcuPrefix(string|null $apcuPrefix): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$apcuPrefix` | **string&#124;null** |  |





***

### getApcuPrefix

The APCu prefix in use, or null if APCu caching is not enabled.

```php
public getApcuPrefix(): string|null
```












***

### register

Registers this instance as an autoloader.

```php
public register(bool $prepend = false): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prepend` | **bool** | Whether to prepend the autoloader or not |





***

### unregister

Unregisters this instance as an autoloader.

```php
public unregister(): void
```












***

### loadClass

Loads the given class or interface.

```php
public loadClass(string $class): true|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | The name of the class |


**Return Value:**

True if loaded, null otherwise




***

### findFile

Finds the path to the file where the class is defined.

```php
public findFile(string $class): string|false
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** | The name of the class |


**Return Value:**

The path if found, false otherwise




***

### getRegisteredLoaders

Returns the currently registered loaders keyed by their corresponding vendor directories.

```php
public static getRegisteredLoaders(): array&lt;string,self&gt;
```



* This method is **static**.








***

### findFileWithExtension



```php
private findFileWithExtension(string $class, string $ext): string|false
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** |  |
| `$ext` | **string** |  |





***

### initializeIncludeClosure



```php
private static initializeIncludeClosure(): void
```



* This method is **static**.








***


***
> Automatically generated on 2025-03-15
