***

# SerializableFieldsTrait

Provides common serialization functionality to fields



* Full name: `\Ramsey\Uuid\Fields\SerializableFieldsTrait`




## Methods


### __construct



```php
public __construct(string $bytes): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bytes` | **string** | The bytes that comprise the fields |





***

### getBytes

Returns the bytes that comprise the fields

```php
public getBytes(): string
```




* This method is **abstract**.







***

### serialize

Returns a string representation of object

```php
public serialize(): string
```












***

### __serialize



```php
public __serialize(): array{bytes: string}
```












***

### unserialize

Constructs the object from a serialized string representation

```php
public unserialize(string $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** | The serialized string representation of the object |





***

### __unserialize



```php
public __unserialize(array{bytes?: string} $data): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **array{bytes?: string}** |  |





***

***
> Automatically generated on 2025-03-18

