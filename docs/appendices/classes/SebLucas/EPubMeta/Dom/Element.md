
# Element

EPUB-specific subclass of DOMElement

Source: https://github.com/splitbrain/php-epub-meta

* Full name: `\SebLucas\EPubMeta\Dom\Element`
* Parent class: [`DOMElement`](../../../DOMElement.md)



## Properties


### namespaces



```php
public static array&lt;string,string&gt; $namespaces
```



* This property is **static**.


***

## Methods


### __construct

Summary of __construct

```php
public __construct(string $name, string $value = &#039;&#039;, string $namespaceUri = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **string** |  |
| `$namespaceUri` | **string** |  |





***

### __get

Summary of __get

```php
public __get(string $name): string|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### __set

Summary of __set

```php
public __set(string $name, mixed $value): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **mixed** |  |





***

### newChild

Create and append a new child

```php
public newChild(string $name, string $value = &#039;&#039;): \SebLucas\EPubMeta\Dom\Element|bool
```

Works with our epub namespaces and omits default namespaces






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **string** |  |





***

### getAttrib

Simple EPUB namespace aware attribute getter

```php
public getAttrib(string $name): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### setAttrib

Simple EPUB namespace aware attribute setter

```php
public setAttrib(string $name, mixed $value): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **mixed** |  |





***

### removeAttrib

Simple EPUB namespace aware attribute remover

```php
public removeAttrib(string $name): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### delete

Remove this node from the DOM

```php
public delete(): void
```












***

### splitQualifiedName

Split given name in namespace prefix and local part

```php
protected splitQualifiedName(string $name): string[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |


**Return Value:**

(prefix, name)




***

### getNameContext



```php
protected getNameContext(string $name): string[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***


***
> Automatically generated on 2025-03-18
