
# ValidatorInterface

A validator validates a string as a proper UUID



* Full name: `\Ramsey\Uuid\Validator\ValidatorInterface`



## Methods


### getPattern

Returns the regular expression pattern used by this validator

```php
public getPattern(): string
```









**Return Value:**

The regular expression pattern this validator uses




***

### validate

Returns true if the provided string represents a UUID

```php
public validate(string $uuid): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uuid` | **string** | The string to validate as a UUID |


**Return Value:**

True if the string is a valid UUID, false otherwise




***


***
> Automatically generated on 2025-03-15
