***

# HTMLPurifier_CSSDefinition

Defines allowed CSS attributes and what their values are.



* Full name: `\HTMLPurifier_CSSDefinition`
* Parent class: [`\HTMLPurifier_Definition`](./HTMLPurifier_Definition.md)

**See Also:**

* \HTMLPurifier_HTMLDefinition - 



## Properties


### type

What type of definition is it?

```php
public $type
```






***

### info

Assoc array of attribute name to definition object.

```php
public $info
```






***

## Methods


### doSetup

Constructs the info array.  The meat of this class.

```php
protected doSetup(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### doSetupProprietary



```php
protected doSetupProprietary(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### doSetupTricky



```php
protected doSetupTricky(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### doSetupTrusted



```php
protected doSetupTrusted(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### setupConfigStuff

Performs extra config-based processing. Based off of
HTMLPurifier_HTMLDefinition.

```php
protected setupConfigStuff(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





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
