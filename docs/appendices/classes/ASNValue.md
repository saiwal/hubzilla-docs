
# ASNValue





* Full name: `\ASNValue`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`TAG_INTEGER`|public| |0x2|
|`TAG_BITSTRING`|public| |0x3|
|`TAG_SEQUENCE`|public| |0x30|

## Properties


### Tag



```php
public $Tag
```






***

### Value



```php
public $Value
```






***

## Methods


### __construct



```php
public __construct(mixed $Tag = 0x0, mixed $Value = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$Tag` | **mixed** |  |
| `$Value` | **mixed** |  |





***

### Encode



```php
public Encode(): mixed
```












***

### Decode



```php
public Decode(mixed& $Buffer): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$Buffer` | **mixed** |  |





***

### ReadBytes



```php
protected static ReadBytes(mixed& $Buffer, mixed $Length): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$Buffer` | **mixed** |  |
| `$Length` | **mixed** |  |





***

### ReadByte



```php
protected static ReadByte(mixed& $Buffer): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$Buffer` | **mixed** |  |





***

### BinToInt



```php
protected static BinToInt(mixed $Bin): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$Bin` | **mixed** |  |





***

### IntToBin



```php
protected static IntToBin(mixed $Int): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$Int` | **mixed** |  |





***

### SetIntBuffer



```php
public SetIntBuffer(mixed $Value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$Value` | **mixed** |  |





***

### GetIntBuffer



```php
public GetIntBuffer(): mixed
```












***

### SetInt



```php
public SetInt(mixed $Value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$Value` | **mixed** |  |





***

### GetInt



```php
public GetInt(): mixed
```












***

### SetSequence



```php
public SetSequence(mixed $Values): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$Values` | **mixed** |  |





***

### GetSequence



```php
public GetSequence(): mixed
```












***


***
> Automatically generated on 2025-03-18
