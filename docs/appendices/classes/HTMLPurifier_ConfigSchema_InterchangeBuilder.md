
# HTMLPurifier_ConfigSchema_InterchangeBuilder





* Full name: `\HTMLPurifier_ConfigSchema_InterchangeBuilder`



## Properties


### varParser

Used for processing DEFAULT, nothing else.

```php
protected $varParser
```






***

## Methods


### __construct



```php
public __construct(\HTMLPurifier_VarParser $varParser = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$varParser` | **\HTMLPurifier_VarParser** |  |





***

### buildFromDirectory



```php
public static buildFromDirectory(string $dir = null): \HTMLPurifier_ConfigSchema_Interchange
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dir` | **string** |  |





***

### buildDir



```php
public buildDir(\HTMLPurifier_ConfigSchema_Interchange $interchange, string $dir = null): \HTMLPurifier_ConfigSchema_Interchange
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$interchange` | **\HTMLPurifier_ConfigSchema_Interchange** |  |
| `$dir` | **string** |  |





***

### buildFile



```php
public buildFile(\HTMLPurifier_ConfigSchema_Interchange $interchange, string $file): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$interchange` | **\HTMLPurifier_ConfigSchema_Interchange** |  |
| `$file` | **string** |  |





***

### build

Builds an interchange object based on a hash.

```php
public build(\HTMLPurifier_ConfigSchema_Interchange $interchange, \HTMLPurifier_StringHash $hash): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$interchange` | **\HTMLPurifier_ConfigSchema_Interchange** | HTMLPurifier_ConfigSchema_Interchange object to build |
| `$hash` | **\HTMLPurifier_StringHash** | source data |




**Throws:**

- [`HTMLPurifier_ConfigSchema_Exception`](./HTMLPurifier_ConfigSchema_Exception.md)



***

### buildDirective



```php
public buildDirective(\HTMLPurifier_ConfigSchema_Interchange $interchange, \HTMLPurifier_StringHash $hash): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$interchange` | **\HTMLPurifier_ConfigSchema_Interchange** |  |
| `$hash` | **\HTMLPurifier_StringHash** |  |




**Throws:**

- [`HTMLPurifier_ConfigSchema_Exception`](./HTMLPurifier_ConfigSchema_Exception.md)



***

### evalArray

Evaluates an array PHP code string without array() wrapper

```php
protected evalArray(string $contents): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$contents` | **string** |  |





***

### lookup

Converts an array list into a lookup array.

```php
protected lookup(array $array): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array` | **array** |  |





***

### id

Convenience function that creates an HTMLPurifier_ConfigSchema_Interchange_Id
object based on a string Id.

```php
protected id(string $id): \HTMLPurifier_ConfigSchema_Interchange_Id
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** |  |





***

### _findUnused

Triggers errors for any unused keys passed in the hash; such keys
may indicate typos, missing values, etc.

```php
protected _findUnused(\HTMLPurifier_StringHash $hash): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hash` | **\HTMLPurifier_StringHash** | Hash to check. |





***


***
> Automatically generated on 2025-03-18
