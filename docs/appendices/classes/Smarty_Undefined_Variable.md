
# Smarty_Undefined_Variable

class for undefined variable object
This class defines an object for undefined variable handling



* Full name: `\Smarty_Undefined_Variable`
* Parent class: [`\Smarty_Variable`](./Smarty_Variable.md)




## Methods


### __get

Returns null for not existing properties

```php
public __get(string $name): null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### __toString

Always returns an empty string.

```php
public __toString(): string
```












***


## Inherited methods


### __construct

create Smarty variable object

```php
public __construct(mixed $value = null, bool $nocache = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **mixed** | the value to assign |
| `$nocache` | **bool** | if true any output of this variable will be not cached |





***

### __toString

<<magic>> String conversion

```php
public __toString(): string
```












***


***
> Automatically generated on 2025-03-18
