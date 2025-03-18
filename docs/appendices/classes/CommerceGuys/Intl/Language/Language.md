
# Language

Represents a language.



* Full name: `\CommerceGuys\Intl\Language\Language`
* This class is marked as **final** and can't be subclassed
* This class is a **Final class**



## Properties


### languageCode

The two-letter language code.

```php
protected string $languageCode
```






***

### name

The language name.

```php
protected string $name
```






***

### locale

The locale (i.e. "en-US").

```php
protected string $locale
```






***

## Methods


### __construct

Creates a new Language instance.

```php
public __construct(array $definition): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$definition` | **array** | The definition array. |





***

### __toString

Returns the string representation of the Language.

```php
public __toString(): string
```












***

### getLanguageCode

Gets the two-letter language code.

```php
public getLanguageCode(): string
```












***

### getName

Gets the language name.

```php
public getName(): string
```

This value is locale specific.










***

### getLocale

Gets the locale.

```php
public getLocale(): string
```

The language name is locale specific.










***


***
> Automatically generated on 2025-03-18
