
# AutonameTest

TestCase for the autoname function



* Full name: `\AutonameTest`
* Parent class: [`TestCase`](./PHPUnit/Framework/TestCase.md)




## Methods


### testAutonameEven

Autonames should be random, even length

```php
public testAutonameEven(): mixed
```












***

### testAutonameOdd

Autonames should be random, odd length

```php
public testAutonameOdd(): mixed
```












***

### testAutonameNoLength

Try to fail autonames

```php
public testAutonameNoLength(): mixed
```












***

### testAutonameNegativeLength

Try to fail it with invalid input

```php
public testAutonameNegativeLength(): mixed
```

TODO: What's corect behaviour here? An exception?










***

### testAutonameLength1

Test with a length, that may be too short
length is maximum - autoname can return something shorter.

```php
public testAutonameLength1(): mixed
```












***


***
> Automatically generated on 2025-03-15
