
# SettingsContainerAbstract





* Full name: `\chillerlan\Settings\SettingsContainerAbstract`
* This class implements:
[`\chillerlan\Settings\SettingsContainerInterface`](./SettingsContainerInterface.md)
* This class is an **Abstract class**




## Methods


### __construct

SettingsContainerAbstract constructor.

```php
public __construct(iterable $properties = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$properties` | **iterable** |  |





***

### construct

calls a method with trait name as replacement constructor for each used trait
(remember pre-php5 classname constructors? yeah, basically this.)

```php
protected construct(): void
```












***

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





***

### jsonSerialize



```php
public jsonSerialize(): array
```












***


***
> Automatically generated on 2025-03-15
