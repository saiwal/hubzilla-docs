
# TimeGeneratorFactory

TimeGeneratorFactory retrieves a default time generator, based on the
environment



* Full name: `\Ramsey\Uuid\Generator\TimeGeneratorFactory`



## Properties


### nodeProvider



```php
private \Ramsey\Uuid\Provider\NodeProviderInterface $nodeProvider
```






***

### timeConverter



```php
private \Ramsey\Uuid\Converter\TimeConverterInterface $timeConverter
```






***

### timeProvider



```php
private \Ramsey\Uuid\Provider\TimeProviderInterface $timeProvider
```






***

## Methods


### __construct



```php
public __construct(\Ramsey\Uuid\Provider\NodeProviderInterface $nodeProvider, \Ramsey\Uuid\Converter\TimeConverterInterface $timeConverter, \Ramsey\Uuid\Provider\TimeProviderInterface $timeProvider): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$nodeProvider` | **\Ramsey\Uuid\Provider\NodeProviderInterface** |  |
| `$timeConverter` | **\Ramsey\Uuid\Converter\TimeConverterInterface** |  |
| `$timeProvider` | **\Ramsey\Uuid\Provider\TimeProviderInterface** |  |





***

### getGenerator

Returns a default time generator, based on the current environment

```php
public getGenerator(): \Ramsey\Uuid\Generator\TimeGeneratorInterface
```












***


***
> Automatically generated on 2025-03-15
