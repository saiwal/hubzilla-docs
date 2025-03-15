***

# HTMLPurifier_ConfigSchema

Configuration definition, defines directives and their defaults.



* Full name: `\HTMLPurifier_ConfigSchema`



## Properties


### defaults

Defaults of the directives and namespaces.

```php
public $defaults
```






***

### defaultPlist

The default property list. Do not edit this property list.

```php
public $defaultPlist
```






***

### info

Definition of the directives.

```php
public $info
```

The structure of this is:

 array(
     'Namespace' => array(
         'Directive' => new stdClass(),
     )
 )

The stdClass may have the following properties:

 - If isAlias isn't set:
     - type: Integer type of directive, see HTMLPurifier_VarParser for definitions
     - allow_null: If set, this directive allows null values
     - aliases: If set, an associative array of value aliases to real values
     - allowed: If set, a lookup array of allowed (string) values
 - If isAlias is set:
     - namespace: Namespace this directive aliases to
     - name: Directive name this directive aliases to

In certain degenerate cases, stdClass will actually be an integer. In
that case, the value is equivalent to an stdClass with the type
property set to the integer. If the integer is negative, type is
equal to the absolute value of integer, and allow_null is true.

This class is friendly with HTMLPurifier_Config. If you need introspection
about the schema, you're better of using the ConfigSchema_Interchange,
which uses more memory but has much richer information.




***

### singleton

Application-wide singleton

```php
protected static $singleton
```



* This property is **static**.


***

## Methods


### __construct



```php
public __construct(): mixed
```












***

### makeFromSerial

Unserializes the default ConfigSchema.

```php
public static makeFromSerial(): \HTMLPurifier_ConfigSchema
```



* This method is **static**.








***

### instance

Retrieves an instance of the application-wide configuration definition.

```php
public static instance(\HTMLPurifier_ConfigSchema $prototype = null): \HTMLPurifier_ConfigSchema
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prototype` | **\HTMLPurifier_ConfigSchema** |  |





***

### add

Defines a directive for configuration

```php
public add(string $key, mixed $default, string $type, bool $allow_null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** | Name of directive |
| `$default` | **mixed** | Default value of directive |
| `$type` | **string** | Allowed type of the directive. See<br />HTMLPurifier_VarParser::$types for allowed values |
| `$allow_null` | **bool** | Whether or not to allow null values |





***

### addValueAliases

Defines a directive value alias.

```php
public addValueAliases(string $key, array $aliases): mixed
```

Directive value aliases are convenient for developers because it lets
them set a directive to several values and get the same result.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** | Name of Directive |
| `$aliases` | **array** | Hash of aliased values to the real alias |





***

### addAllowedValues

Defines a set of allowed values for a directive.

```php
public addAllowedValues(string $key, array $allowed): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** | Name of directive |
| `$allowed` | **array** | Lookup array of allowed values |





***

### addAlias

Defines a directive alias for backwards compatibility

```php
public addAlias(string $key, string $new_key): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** | Directive that will be aliased |
| `$new_key` | **string** | Directive that the alias will be to |





***

### postProcess

Replaces any stdClass that only has the type property with type integer.

```php
public postProcess(): mixed
```












***


***
> Automatically generated on 2025-03-15
