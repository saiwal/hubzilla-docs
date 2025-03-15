
# HTMLPurifier_ConfigSchema_Builder_Xml

Converts HTMLPurifier_ConfigSchema_Interchange to an XML format,
which can be further processed to generate documentation.



* Full name: `\HTMLPurifier_ConfigSchema_Builder_Xml`
* Parent class: [`XMLWriter`](./XMLWriter.md)



## Properties


### interchange



```php
protected $interchange
```






***

### namespace



```php
private $namespace
```






***

## Methods


### writeHTMLDiv



```php
protected writeHTMLDiv(string $html): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string** |  |





***

### export



```php
protected export(mixed $var): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$var` | **mixed** |  |





***

### build



```php
public build(\HTMLPurifier_ConfigSchema_Interchange $interchange): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$interchange` | **\HTMLPurifier_ConfigSchema_Interchange** |  |





***

### buildDirective



```php
public buildDirective(\HTMLPurifier_ConfigSchema_Interchange_Directive $directive): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$directive` | **\HTMLPurifier_ConfigSchema_Interchange_Directive** |  |





***


***
> Automatically generated on 2025-03-15
