***

# LibXMLException

This exception is thrown when the Reader runs into a parsing error.

This exception effectively wraps 1 or more LibXMLError objects.

* Full name: `\Sabre\Xml\LibXMLException`
* Parent class: [`\Sabre\Xml\ParseException`](./ParseException.md)



## Properties


### errors

The error list.

```php
protected \LibXMLError[] $errors
```






***

## Methods


### __construct

Creates the exception.

```php
public __construct(\LibXMLError[] $errors, int $code, \Throwable $previousException = null): mixed
```

You should pass a list of LibXMLError objects in its constructor.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$errors` | **\LibXMLError[]** |  |
| `$code` | **int** |  |
| `$previousException` | **\Throwable** |  |





***

### getErrors

Returns the LibXML errors.

```php
public getErrors(): array
```












***


***
> Automatically generated on 2025-03-15
