***

# BitBuffer

Holds the raw binary data



* Full name: `\chillerlan\QRCode\Helpers\BitBuffer`
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**



## Properties


### buffer

The buffer content

```php
protected int[] $buffer
```






***

### length

Length of the content (bits)

```php
protected int $length
```






***

## Methods


### clear

clears the buffer

```php
public clear(): \chillerlan\QRCode\Helpers\BitBuffer
```












***

### put

appends a sequence of bits

```php
public put(int $num, int $length): \chillerlan\QRCode\Helpers\BitBuffer
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$num` | **int** |  |
| `$length` | **int** |  |





***

### putBit

appends a single bit

```php
public putBit(bool $bit): \chillerlan\QRCode\Helpers\BitBuffer
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bit` | **bool** |  |





***

### getLength

returns the current buffer length

```php
public getLength(): int
```












***

### getBuffer

returns the buffer content

```php
public getBuffer(): array
```












***


***
> Automatically generated on 2025-03-15
