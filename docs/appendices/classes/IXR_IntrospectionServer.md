
# IXR_IntrospectionServer

IXR_IntrospectionServer



* Full name: `\IXR_IntrospectionServer`
* Parent class: [`\IXR_Server`](./IXR_Server.md)



## Properties


### signatures



```php
public $signatures
```






***

### help



```php
public $help
```






***

## Methods


### __construct



```php
public __construct(): mixed
```












***

### addCallback



```php
public addCallback(mixed $method, mixed $callback, mixed $args, mixed $help): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$method` | **mixed** |  |
| `$callback` | **mixed** |  |
| `$args` | **mixed** |  |
| `$help` | **mixed** |  |





***

### call



```php
public call(mixed $methodname, mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$methodname` | **mixed** |  |
| `$args` | **mixed** |  |





***

### methodSignature



```php
public methodSignature(mixed $method): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$method` | **mixed** |  |





***

### methodHelp



```php
public methodHelp(mixed $method): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$method` | **mixed** |  |





***


## Inherited methods


### __construct



```php
public __construct(mixed $callbacks = false, mixed $data = false, mixed $wait = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$callbacks` | **mixed** |  |
| `$data` | **mixed** |  |
| `$wait` | **mixed** |  |





***

### serve



```php
public serve(mixed $data = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |





***

### call



```php
public call(mixed $methodname, mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$methodname` | **mixed** |  |
| `$args` | **mixed** |  |





***

### error



```php
public error(mixed $error, mixed $message = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$error` | **mixed** |  |
| `$message` | **mixed** |  |





***

### output



```php
public output(mixed $xml): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$xml` | **mixed** |  |





***

### hasMethod



```php
public hasMethod(mixed $method): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$method` | **mixed** |  |





***

### setCapabilities



```php
public setCapabilities(): mixed
```












***

### getCapabilities



```php
public getCapabilities(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### setCallbacks



```php
public setCallbacks(): mixed
```












***

### listMethods



```php
public listMethods(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### multiCall



```php
public multiCall(mixed $methodcalls): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$methodcalls` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
