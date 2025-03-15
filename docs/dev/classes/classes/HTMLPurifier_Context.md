***

# HTMLPurifier_Context

Registry object that contains information about the current context.



* Full name: `\HTMLPurifier_Context`



## Properties


### _storage

Private array that stores the references.

```php
private $_storage
```






***

## Methods


### register

Registers a variable into the context.

```php
public register(string $name, mixed& $ref): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | String name |
| `$ref` | **mixed** | Reference to variable to be registered |





***

### get

Retrieves a variable reference from the context.

```php
public get(string $name, bool $ignore_error = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | String name |
| `$ignore_error` | **bool** | Boolean whether or not to ignore error |





***

### destroy

Destroys a variable in the context.

```php
public destroy(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | String name |





***

### exists

Checks whether or not the variable exists.

```php
public exists(string $name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | String name |





***

### loadArray

Loads a series of variables from an associative array

```php
public loadArray(array $context_array): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$context_array` | **array** | Assoc array of variables to load |





***


***
> Automatically generated on 2025-03-15
