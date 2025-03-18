
# FeatureSet

FeatureSet detects and exposes available features in the current environment

A feature set is used by UuidFactory to determine the available features and
capabilities of the environment.

* Full name: `\Ramsey\Uuid\FeatureSet`



## Properties


### timeProvider



```php
private ?\Ramsey\Uuid\Provider\TimeProviderInterface $timeProvider
```






***

### calculator



```php
private \Ramsey\Uuid\Math\CalculatorInterface $calculator
```






***

### codec



```php
private \Ramsey\Uuid\Codec\CodecInterface $codec
```






***

### dceSecurityGenerator



```php
private \Ramsey\Uuid\Generator\DceSecurityGeneratorInterface $dceSecurityGenerator
```






***

### nameGenerator



```php
private \Ramsey\Uuid\Generator\NameGeneratorInterface $nameGenerator
```






***

### nodeProvider



```php
private \Ramsey\Uuid\Provider\NodeProviderInterface $nodeProvider
```






***

### numberConverter



```php
private \Ramsey\Uuid\Converter\NumberConverterInterface $numberConverter
```






***

### randomGenerator



```php
private \Ramsey\Uuid\Generator\RandomGeneratorInterface $randomGenerator
```






***

### timeConverter



```php
private \Ramsey\Uuid\Converter\TimeConverterInterface $timeConverter
```






***

### timeGenerator



```php
private \Ramsey\Uuid\Generator\TimeGeneratorInterface $timeGenerator
```






***

### unixTimeGenerator



```php
private \Ramsey\Uuid\Generator\TimeGeneratorInterface $unixTimeGenerator
```






***

### builder



```php
private \Ramsey\Uuid\Builder\UuidBuilderInterface $builder
```






***

### validator



```php
private \Ramsey\Uuid\Validator\ValidatorInterface $validator
```






***

### force32Bit



```php
private bool $force32Bit
```






***

### ignoreSystemNode



```php
private bool $ignoreSystemNode
```






***

### enablePecl



```php
private bool $enablePecl
```






***

## Methods


### __construct



```php
public __construct(bool $useGuids = false, bool $force32Bit = false, bool $forceNoBigNumber = false, bool $ignoreSystemNode = false, bool $enablePecl = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$useGuids` | **bool** | True build UUIDs using the GuidStringCodec |
| `$force32Bit` | **bool** | True to force the use of 32-bit functionality<br />(primarily for testing purposes) |
| `$forceNoBigNumber` | **bool** | (obsolete) |
| `$ignoreSystemNode` | **bool** | True to disable attempts to check for the<br />system node ID (primarily for testing purposes) |
| `$enablePecl` | **bool** | True to enable the use of the PeclUuidTimeGenerator<br />to generate version 1 UUIDs |





***

### getBuilder

Returns the builder configured for this environment

```php
public getBuilder(): \Ramsey\Uuid\Builder\UuidBuilderInterface
```












***

### getCalculator

Returns the calculator configured for this environment

```php
public getCalculator(): \Ramsey\Uuid\Math\CalculatorInterface
```












***

### getCodec

Returns the codec configured for this environment

```php
public getCodec(): \Ramsey\Uuid\Codec\CodecInterface
```












***

### getDceSecurityGenerator

Returns the DCE Security generator configured for this environment

```php
public getDceSecurityGenerator(): \Ramsey\Uuid\Generator\DceSecurityGeneratorInterface
```












***

### getNameGenerator

Returns the name generator configured for this environment

```php
public getNameGenerator(): \Ramsey\Uuid\Generator\NameGeneratorInterface
```












***

### getNodeProvider

Returns the node provider configured for this environment

```php
public getNodeProvider(): \Ramsey\Uuid\Provider\NodeProviderInterface
```












***

### getNumberConverter

Returns the number converter configured for this environment

```php
public getNumberConverter(): \Ramsey\Uuid\Converter\NumberConverterInterface
```












***

### getRandomGenerator

Returns the random generator configured for this environment

```php
public getRandomGenerator(): \Ramsey\Uuid\Generator\RandomGeneratorInterface
```












***

### getTimeConverter

Returns the time converter configured for this environment

```php
public getTimeConverter(): \Ramsey\Uuid\Converter\TimeConverterInterface
```












***

### getTimeGenerator

Returns the time generator configured for this environment

```php
public getTimeGenerator(): \Ramsey\Uuid\Generator\TimeGeneratorInterface
```












***

### getUnixTimeGenerator

Returns the Unix Epoch time generator configured for this environment

```php
public getUnixTimeGenerator(): \Ramsey\Uuid\Generator\TimeGeneratorInterface
```












***

### getValidator

Returns the validator configured for this environment

```php
public getValidator(): \Ramsey\Uuid\Validator\ValidatorInterface
```












***

### setCalculator

Sets the calculator to use in this environment

```php
public setCalculator(\Ramsey\Uuid\Math\CalculatorInterface $calculator): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calculator` | **\Ramsey\Uuid\Math\CalculatorInterface** |  |





***

### setDceSecurityProvider

Sets the DCE Security provider to use in this environment

```php
public setDceSecurityProvider(\Ramsey\Uuid\Provider\DceSecurityProviderInterface $dceSecurityProvider): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dceSecurityProvider` | **\Ramsey\Uuid\Provider\DceSecurityProviderInterface** |  |





***

### setNodeProvider

Sets the node provider to use in this environment

```php
public setNodeProvider(\Ramsey\Uuid\Provider\NodeProviderInterface $nodeProvider): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$nodeProvider` | **\Ramsey\Uuid\Provider\NodeProviderInterface** |  |





***

### setTimeProvider

Sets the time provider to use in this environment

```php
public setTimeProvider(\Ramsey\Uuid\Provider\TimeProviderInterface $timeProvider): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$timeProvider` | **\Ramsey\Uuid\Provider\TimeProviderInterface** |  |





***

### setValidator

Set the validator to use in this environment

```php
public setValidator(\Ramsey\Uuid\Validator\ValidatorInterface $validator): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$validator` | **\Ramsey\Uuid\Validator\ValidatorInterface** |  |





***

### buildCodec

Returns a codec configured for this environment

```php
private buildCodec(bool $useGuids = false): \Ramsey\Uuid\Codec\CodecInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$useGuids` | **bool** | Whether to build UUIDs using the GuidStringCodec |





***

### buildDceSecurityGenerator

Returns a DCE Security generator configured for this environment

```php
private buildDceSecurityGenerator(\Ramsey\Uuid\Provider\DceSecurityProviderInterface $dceSecurityProvider): \Ramsey\Uuid\Generator\DceSecurityGeneratorInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dceSecurityProvider` | **\Ramsey\Uuid\Provider\DceSecurityProviderInterface** |  |





***

### buildNodeProvider

Returns a node provider configured for this environment

```php
private buildNodeProvider(): \Ramsey\Uuid\Provider\NodeProviderInterface
```












***

### buildNumberConverter

Returns a number converter configured for this environment

```php
private buildNumberConverter(\Ramsey\Uuid\Math\CalculatorInterface $calculator): \Ramsey\Uuid\Converter\NumberConverterInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calculator` | **\Ramsey\Uuid\Math\CalculatorInterface** |  |





***

### buildRandomGenerator

Returns a random generator configured for this environment

```php
private buildRandomGenerator(): \Ramsey\Uuid\Generator\RandomGeneratorInterface
```












***

### buildTimeGenerator

Returns a time generator configured for this environment

```php
private buildTimeGenerator(\Ramsey\Uuid\Provider\TimeProviderInterface $timeProvider): \Ramsey\Uuid\Generator\TimeGeneratorInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$timeProvider` | **\Ramsey\Uuid\Provider\TimeProviderInterface** | The time provider to use with<br />the time generator |





***

### buildUnixTimeGenerator

Returns a Unix Epoch time generator configured for this environment

```php
private buildUnixTimeGenerator(): \Ramsey\Uuid\Generator\TimeGeneratorInterface
```












***

### buildNameGenerator

Returns a name generator configured for this environment

```php
private buildNameGenerator(): \Ramsey\Uuid\Generator\NameGeneratorInterface
```












***

### buildTimeConverter

Returns a time converter configured for this environment

```php
private buildTimeConverter(\Ramsey\Uuid\Math\CalculatorInterface $calculator): \Ramsey\Uuid\Converter\TimeConverterInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calculator` | **\Ramsey\Uuid\Math\CalculatorInterface** |  |





***

### buildUuidBuilder

Returns a UUID builder configured for this environment

```php
private buildUuidBuilder(bool $useGuids = false): \Ramsey\Uuid\Builder\UuidBuilderInterface
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$useGuids` | **bool** | Whether to build UUIDs using the GuidStringCodec |





***

### is64BitSystem

Returns true if the PHP build is 64-bit

```php
private is64BitSystem(): bool
```












***


***
> Automatically generated on 2025-03-18
