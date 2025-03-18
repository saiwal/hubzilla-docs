
# HTMLPurifier_VarParser_Flexible

Performs safe variable parsing based on types which can be used by
users. This may not be able to represent all possible data inputs,
however.



* Full name: `\HTMLPurifier_VarParser_Flexible`
* Parent class: [`\HTMLPurifier_VarParser`](./HTMLPurifier_VarParser.md)




## Methods


### parseImplementation

Actually implements the parsing. Base implementation does not
do anything to $var. Subclasses should overload this!

```php
protected parseImplementation(mixed $var, int $type, bool $allow_null): array|bool|float|int|mixed|null|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$var` | **mixed** |  |
| `$type` | **int** |  |
| `$allow_null` | **bool** |  |




**Throws:**

- [`HTMLPurifier_VarParserException`](./HTMLPurifier_VarParserException.md)



***


## Inherited methods


### parse

Validate a variable according to type.

```php
final public parse(mixed $var, int $type, bool $allow_null = false): string
```

It may return NULL as a valid type if $allow_null is true.



* This method is **final**.


**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$var` | **mixed** | Variable to validate |
| `$type` | **int** | Type of variable, see HTMLPurifier_VarParser-&gt;types |
| `$allow_null` | **bool** | Whether or not to permit null as a value |


**Return Value:**

Validated and type-coerced variable



**Throws:**

- [`HTMLPurifier_VarParserException`](./HTMLPurifier_VarParserException.md)



***

### parseImplementation

Actually implements the parsing. Base implementation does not
do anything to $var. Subclasses should overload this!

```php
protected parseImplementation(mixed $var, int $type, bool $allow_null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$var` | **mixed** |  |
| `$type` | **int** |  |
| `$allow_null` | **bool** |  |





***

### error

Throws an exception.

```php
protected error(mixed $msg): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$msg` | **mixed** |  |




**Throws:**

- [`HTMLPurifier_VarParserException`](./HTMLPurifier_VarParserException.md)



***

### errorInconsistent

Throws an inconsistency exception.

```php
protected errorInconsistent(string $class, int $type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$class` | **string** |  |
| `$type` | **int** |  |




**Throws:**

- [`HTMLPurifier_Exception`](./HTMLPurifier_Exception.md)



***

### errorGeneric

Generic error for if a type didn't work.

```php
protected errorGeneric(mixed $var, int $type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$var` | **mixed** |  |
| `$type` | **int** |  |





***

### getTypeName



```php
public static getTypeName(int $type): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **int** |  |





***


***
> Automatically generated on 2025-03-18
