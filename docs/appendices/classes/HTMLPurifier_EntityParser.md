
# HTMLPurifier_EntityParser

Handles referencing and derefencing character entities



* Full name: `\HTMLPurifier_EntityParser`



## Properties


### _entity_lookup

Reference to entity lookup table.

```php
protected $_entity_lookup
```






***

### _textEntitiesRegex

Callback regex string for entities in text.

```php
protected $_textEntitiesRegex
```






***

### _attrEntitiesRegex

Callback regex string for entities in attributes.

```php
protected $_attrEntitiesRegex
```






***

### _semiOptionalPrefixRegex

Tests if the beginning of a string is a semi-optional regex

```php
protected $_semiOptionalPrefixRegex
```






***

### _substituteEntitiesRegex

Callback regex string for parsing entities.

```php
protected $_substituteEntitiesRegex
```






***

### _special_dec2str

Decimal to parsed string conversion table for special entities.

```php
protected $_special_dec2str
```






***

### _special_ent2dec

Stripped entity names to decimal conversion table for special entities.

```php
protected $_special_ent2dec
```






***

## Methods


### __construct



```php
public __construct(): mixed
```












***

### substituteTextEntities

Substitute entities with the parsed equivalents.  Use this on
textual data in an HTML document (as opposed to attributes.)

```php
public substituteTextEntities(string $string): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | String to have entities parsed. |


**Return Value:**

Parsed string.




***

### substituteAttrEntities

Substitute entities with the parsed equivalents.  Use this on
attribute contents in documents.

```php
public substituteAttrEntities(string $string): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | String to have entities parsed. |


**Return Value:**

Parsed string.




***

### entityCallback

Callback function for substituteNonSpecialEntities() that does the work.

```php
protected entityCallback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** | PCRE matches array, with 0 the entire match, and<br />either index 1, 2 or 3 set with a hex value, dec value,<br />or string (respectively). |


**Return Value:**

Replacement string.




***

### substituteNonSpecialEntities

Substitutes non-special entities with their parsed equivalents. Since
running this whenever you have parsed character is t3h 5uck, we run
it before everything else.

```php
public substituteNonSpecialEntities(string $string): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | String to have non-special entities parsed. |


**Return Value:**

Parsed string.




***

### nonSpecialEntityCallback

Callback function for substituteNonSpecialEntities() that does the work.

```php
protected nonSpecialEntityCallback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** | PCRE matches array, with 0 the entire match, and<br />either index 1, 2 or 3 set with a hex value, dec value,<br />or string (respectively). |


**Return Value:**

Replacement string.




***

### substituteSpecialEntities

Substitutes only special entities with their parsed equivalents.

```php
public substituteSpecialEntities(string $string): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | String to have non-special entities parsed. |


**Return Value:**

Parsed string.




***

### specialEntityCallback

Callback function for substituteSpecialEntities() that does the work.

```php
protected specialEntityCallback(array $matches): string
```

This callback has same syntax as nonSpecialEntityCallback().






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** | PCRE-style matches array, with 0 the entire match, and<br />either index 1, 2 or 3 set with a hex value, dec value,<br />or string (respectively). |


**Return Value:**

Replacement string.




***


***
> Automatically generated on 2025-03-18
