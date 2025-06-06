
# LogoOptions

The QRCode settings container



* Full name: `\chillerlan\QRCodeExamples\LogoOptions`
* Parent class: [`\chillerlan\QRCode\QROptions`](../QRCode/QROptions.md)



## Properties


### logoSpaceWidth



```php
protected int $logoSpaceWidth
```






***

### logoSpaceHeight



```php
protected int $logoSpaceHeight
```






***



## Inherited methods


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

### setMinMaxVersion

clamp min/max version number

```php
protected setMinMaxVersion(int $versionMin, int $versionMax): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$versionMin` | **int** |  |
| `$versionMax` | **int** |  |





***

### set_versionMin

sets the minimum version number

```php
protected set_versionMin(int $version): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$version` | **int** |  |





***

### set_versionMax

sets the maximum version number

```php
protected set_versionMax(int $version): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$version` | **int** |  |





***

### set_eccLevel

sets the error correction level

```php
protected set_eccLevel(int $eccLevel): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$eccLevel` | **int** |  |




**Throws:**

- [`QRCodeException`](../QRCode/QRCodeException.md)



***

### set_maskPattern

sets/clamps the mask pattern

```php
protected set_maskPattern(int $maskPattern): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$maskPattern` | **int** |  |





***

### set_imageTransparencyBG

sets the transparency background color

```php
protected set_imageTransparencyBG(array $imageTransparencyBG): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$imageTransparencyBG` | **array** |  |




**Throws:**

- [`QRCodeException`](../QRCode/QRCodeException.md)



***

### set_version

sets/clamps the version number

```php
protected set_version(int $version): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$version` | **int** |  |





***

### set_fpdfMeasureUnit

sets the FPDF measurement unit

```php
protected set_fpdfMeasureUnit(string $unit): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$unit` | **string** |  |





***


***
> Automatically generated on 2025-03-18
