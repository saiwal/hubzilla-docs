
# HTMLPurifier_URIDefinition

Super-class for definition datatype objects, implements serialization
functions for the class.



* Full name: `\HTMLPurifier_URIDefinition`
* Parent class: [`\HTMLPurifier_Definition`](./HTMLPurifier_Definition.md)



## Properties


### type

What type of definition is it?

```php
public $type
```






***

### filters



```php
protected $filters
```






***

### postFilters



```php
protected $postFilters
```






***

### registeredFilters



```php
protected $registeredFilters
```






***

### base

HTMLPurifier_URI object of the base specified at %URI.Base

```php
public $base
```






***

### host

String host to consider "home" base, derived off of $base

```php
public $host
```






***

### defaultScheme

Name of default scheme based on %URI.DefaultScheme and %URI.Base

```php
public $defaultScheme
```






***

## Methods


### __construct



```php
public __construct(): mixed
```












***

### registerFilter



```php
public registerFilter(mixed $filter): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filter` | **mixed** |  |





***

### addFilter



```php
public addFilter(mixed $filter, mixed $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filter` | **mixed** |  |
| `$config` | **mixed** |  |





***

### doSetup

Sets up the definition object into the final form, something
not done by the constructor

```php
protected doSetup(mixed $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **mixed** |  |





***

### setupFilters



```php
protected setupFilters(mixed $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **mixed** |  |





***

### setupMemberVariables



```php
protected setupMemberVariables(mixed $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **mixed** |  |





***

### getDefaultScheme



```php
public getDefaultScheme(mixed $config, mixed $context): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **mixed** |  |
| `$context` | **mixed** |  |





***

### filter



```php
public filter(mixed& $uri, mixed $config, mixed $context): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **mixed** |  |
| `$config` | **mixed** |  |
| `$context` | **mixed** |  |





***

### postFilter



```php
public postFilter(mixed& $uri, mixed $config, mixed $context): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **mixed** |  |
| `$config` | **mixed** |  |
| `$context` | **mixed** |  |





***


## Inherited methods


### doSetup

Sets up the definition object into the final form, something
not done by the constructor

```php
protected doSetup(\HTMLPurifier_Config $config): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### setup

Setup function that aborts if already setup

```php
public setup(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***


***
> Automatically generated on 2025-03-15
