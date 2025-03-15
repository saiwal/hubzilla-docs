***

# IXR_ClassServer

Extension of the {@link IXR_Server} class to easily wrap objects.

Class is designed to extend the existing XML-RPC server to allow the
presentation of methods from a variety of different objects via an
XML-RPC server.
It is intended to assist in organization of your XML-RPC methods by allowing
you to "write once" in your existing model classes and present them.

* Full name: `\IXR_ClassServer`
* Parent class: [`\IXR_Server`](./IXR_Server.md)



## Properties


### _objects



```php
public $_objects
```






***

### _delim



```php
public $_delim
```






***

## Methods


### __construct



```php
public __construct(mixed $delim = &#039;.&#039;, mixed $wait = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$delim` | **mixed** |  |
| `$wait` | **mixed** |  |





***

### addMethod



```php
public addMethod(mixed $rpcName, mixed $functionName): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rpcName` | **mixed** |  |
| `$functionName` | **mixed** |  |





***

### registerObject



```php
public registerObject(mixed $object, mixed $methods, mixed $prefix = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$object` | **mixed** |  |
| `$methods` | **mixed** |  |
| `$prefix` | **mixed** |  |





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
> Automatically generated on 2025-03-15
