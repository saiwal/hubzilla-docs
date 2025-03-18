
# HTMLPurifier_ConfigSchema_Interchange

Generic schema interchange format that can be converted to a runtime
representation (HTMLPurifier_ConfigSchema) or HTML documentation. Members
are completely validated.



* Full name: `\HTMLPurifier_ConfigSchema_Interchange`



## Properties


### name

Name of the application this schema is describing.

```php
public $name
```






***

### directives

Array of Directive ID => array(directive info)

```php
public $directives
```






***

## Methods


### addDirective

Adds a directive array to $directives

```php
public addDirective(\HTMLPurifier_ConfigSchema_Interchange_Directive $directive): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$directive` | **\HTMLPurifier_ConfigSchema_Interchange_Directive** |  |




**Throws:**

- [`HTMLPurifier_ConfigSchema_Exception`](./HTMLPurifier_ConfigSchema_Exception.md)



***

### validate

Convenience function to perform standard validation. Throws exception
on failed validation.

```php
public validate(): mixed
```












***


***
> Automatically generated on 2025-03-18
