
# SettingsContainerInterface

a generic container with magic getter and setter



* Full name: `\chillerlan\Settings\SettingsContainerInterface`
* Parent interfaces: [`JsonSerializable`](../../JsonSerializable.md)


## Methods


### __get

Retrieve the value of $property

```php
public __get(string $property): mixed|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$property` | **string** |  |





***

### __set

Set $property to $value while avoiding private and non-existing properties

```php
public __set(string $property, mixed $value): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$property` | **string** |  |
| `$value` | **mixed** |  |





***

### __isset

Checks if $property is set (aka. not null), excluding private properties

```php
public __isset(string $property): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$property` | **string** |  |





***

### __unset

Unsets $property while avoiding private and non-existing properties

```php
public __unset(string $property): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$property` | **string** |  |





***

### __toString



```php
public __toString(): string
```












**See Also:**

* \chillerlan\Settings\SettingsContainerInterface::toJSON() - 

***

### toArray

Returns an array representation of the settings object

```php
public toArray(): array
```












***

### fromIterable

Sets properties from a given iterable

```php
public fromIterable(iterable $properties): \chillerlan\Settings\SettingsContainerInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$properties` | **iterable** |  |





***

### toJSON

Returns a JSON representation of the settings object

```php
public toJSON(int $jsonOptions = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$jsonOptions` | **int** |  |





**See Also:**

* \json_encode() - 

***

### fromJSON

Sets properties from a given JSON string

```php
public fromJSON(string $json): \chillerlan\Settings\SettingsContainerInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$json` | **string** |  |




**Throws:**

- [`Exception`](../../Exception.md)

- [`JsonException`](../../JsonException.md)



***


***
> Automatically generated on 2025-03-18
