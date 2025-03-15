
# GenericValidator

GenericValidator validates strings as UUIDs of any variant



* Full name: `\Ramsey\Uuid\Validator\GenericValidator`
* This class is marked as **final** and can't be subclassed
* This class implements:
[`\Ramsey\Uuid\Validator\ValidatorInterface`](./ValidatorInterface.md)
* This class is a **Final class**


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`VALID_PATTERN`|private| |&#039;\A[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{12}\z&#039;|


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
