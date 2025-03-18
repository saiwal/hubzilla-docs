
# Receiver





* Full name: `\Zotlabs\Zot6\Receiver`



## Properties


### data



```php
protected $data
```






***

### encrypted



```php
protected $encrypted
```






***

### error



```php
protected $error
```






***

### messagetype



```php
protected $messagetype
```






***

### sender



```php
protected $sender
```






***

### site_id



```php
protected $site_id
```






***

### validated



```php
protected $validated
```






***

### recipients



```php
protected $recipients
```






***

### response



```php
protected $response
```






***

### handler



```php
protected $handler
```






***

### prvkey



```php
protected $prvkey
```






***

### rawdata



```php
protected $rawdata
```






***

### sigdata



```php
protected $sigdata
```






***

### hub



```php
protected $hub
```






***

## Methods


### __construct



```php
public __construct(mixed $handler, mixed $localdata = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$handler` | **mixed** |  |
| `$localdata` | **mixed** |  |





***

### run



```php
public run(): mixed
```












***

### ValidateSender



```php
public ValidateSender(): mixed
```












***

### Valid_Httpsig



```php
public Valid_Httpsig(): mixed
```












***

### Dispatch



```php
public Dispatch(): mixed
```












***

### EncryptResponse



```php
public EncryptResponse(): mixed
```












***


***
> Automatically generated on 2025-03-18
