
# HTMLPurifier_ConfigSchema_Interchange_Directive

Interchange component class describing configuration directives.



* Full name: `\HTMLPurifier_ConfigSchema_Interchange_Directive`



## Properties


### id

ID of directive.

```php
public $id
```






***

### type

Type, e.g. 'integer' or 'istring'.

```php
public $type
```






***

### default

Default value, e.g. 3 or 'DefaultVal'.

```php
public $default
```






***

### description

HTML description.

```php
public $description
```






***

### typeAllowsNull

Whether or not null is allowed as a value.

```php
public $typeAllowsNull
```






***

### allowed

Lookup table of allowed scalar values.

```php
public $allowed
```

e.g. array('allowed' => true).
Null if all values are allowed.




***

### aliases

List of aliases for the directive.

```php
public $aliases
```

e.g. array(new HTMLPurifier_ConfigSchema_Interchange_Id('Ns', 'Dir'))).




***

### valueAliases

Hash of value aliases, e.g. array('alt' => 'real'). Null if value
aliasing is disabled (necessary for non-scalar types).

```php
public $valueAliases
```






***

### version

Version of HTML Purifier the directive was introduced, e.g. '1.3.1'.

```php
public $version
```

Null if the directive has always existed.




***

### deprecatedUse

ID of directive that supercedes this old directive.

```php
public $deprecatedUse
```

Null if not deprecated.




***

### deprecatedVersion

Version of HTML Purifier this directive was deprecated. Null if not
deprecated.

```php
public $deprecatedVersion
```






***

### external

List of external projects this directive depends on, e.g. array('CSSTidy').

```php
public $external
```






***



***
> Automatically generated on 2025-03-15
