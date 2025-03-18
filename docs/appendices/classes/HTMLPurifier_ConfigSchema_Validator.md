
# HTMLPurifier_ConfigSchema_Validator

Performs validations on HTMLPurifier_ConfigSchema_Interchange



* Full name: `\HTMLPurifier_ConfigSchema_Validator`



## Properties


### interchange



```php
protected $interchange
```






***

### aliases



```php
protected $aliases
```






***

### context

Context-stack to provide easy to read error messages.

```php
protected $context
```






***

### parser

to test default's type.

```php
protected $parser
```






***

## Methods


### __construct



```php
public __construct(): mixed
```












***

### validate

Validates a fully-formed interchange object.

```php
public validate(\HTMLPurifier_ConfigSchema_Interchange $interchange): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$interchange` | **\HTMLPurifier_ConfigSchema_Interchange** |  |





***

### validateId

Validates a HTMLPurifier_ConfigSchema_Interchange_Id object.

```php
public validateId(\HTMLPurifier_ConfigSchema_Interchange_Id $id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **\HTMLPurifier_ConfigSchema_Interchange_Id** |  |





***

### validateDirective

Validates a HTMLPurifier_ConfigSchema_Interchange_Directive object.

```php
public validateDirective(\HTMLPurifier_ConfigSchema_Interchange_Directive $d): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$d` | **\HTMLPurifier_ConfigSchema_Interchange_Directive** |  |





***

### validateDirectiveAllowed

Extra validation if $allowed member variable of
HTMLPurifier_ConfigSchema_Interchange_Directive is defined.

```php
public validateDirectiveAllowed(\HTMLPurifier_ConfigSchema_Interchange_Directive $d): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$d` | **\HTMLPurifier_ConfigSchema_Interchange_Directive** |  |





***

### validateDirectiveValueAliases

Extra validation if $valueAliases member variable of
HTMLPurifier_ConfigSchema_Interchange_Directive is defined.

```php
public validateDirectiveValueAliases(\HTMLPurifier_ConfigSchema_Interchange_Directive $d): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$d` | **\HTMLPurifier_ConfigSchema_Interchange_Directive** |  |





***

### validateDirectiveAliases

Extra validation if $aliases member variable of
HTMLPurifier_ConfigSchema_Interchange_Directive is defined.

```php
public validateDirectiveAliases(\HTMLPurifier_ConfigSchema_Interchange_Directive $d): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$d` | **\HTMLPurifier_ConfigSchema_Interchange_Directive** |  |





***

### with

Convenience function for generating HTMLPurifier_ConfigSchema_ValidatorAtom
for validating simple member variables of objects.

```php
protected with(mixed $obj, mixed $member): \HTMLPurifier_ConfigSchema_ValidatorAtom
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **mixed** |  |
| `$member` | **mixed** |  |





***

### error

Emits an error, providing helpful context.

```php
protected error(mixed $target, mixed $msg): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$target` | **mixed** |  |
| `$msg` | **mixed** |  |




**Throws:**

- [`HTMLPurifier_ConfigSchema_Exception`](./HTMLPurifier_ConfigSchema_Exception.md)



***

### getFormattedContext

Returns a formatted context string.

```php
protected getFormattedContext(): string
```












***


***
> Automatically generated on 2025-03-18
