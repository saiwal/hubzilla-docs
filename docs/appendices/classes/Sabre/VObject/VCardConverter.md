
# VCardConverter

This utility converts vcards from one version to another.



* Full name: `\Sabre\VObject\VCardConverter`




## Methods


### convert

Converts a vCard object to a new version.

```php
public convert(\Sabre\VObject\Component\VCard $input, int $targetVersion): mixed
```

targetVersion must be one of:
  Document::VCARD21
  Document::VCARD30
  Document::VCARD40

Currently only 3.0 and 4.0 as input and output versions.

2.1 has some minor support for the input version, it's incomplete at the
moment though.

If input and output version are identical, a clone is returned.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **\Sabre\VObject\Component\VCard** |  |
| `$targetVersion` | **int** |  |





***

### convertProperty

Handles conversion of a single property.

```php
protected convertProperty(\Sabre\VObject\Component\VCard $input, \Sabre\VObject\Component\VCard $output, \Sabre\VObject\Property $property, int $targetVersion): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **\Sabre\VObject\Component\VCard** |  |
| `$output` | **\Sabre\VObject\Component\VCard** |  |
| `$property` | **\Sabre\VObject\Property** |  |
| `$targetVersion` | **int** |  |





***

### convertBinaryToUri

Converts a BINARY property to a URI property.

```php
protected convertBinaryToUri(\Sabre\VObject\Component\VCard $output, \Sabre\VObject\Property\Binary $newProperty, mixed& $parameters): \Sabre\VObject\Property\Uri
```

vCard 4.0 no longer supports BINARY properties.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$output` | **\Sabre\VObject\Component\VCard** |  |
| `$newProperty` | **\Sabre\VObject\Property\Binary** |  |
| `$parameters` | **mixed** | list of parameters that will eventually be added to<br />the new property |





***

### convertUriToBinary

Converts a URI property to a BINARY property.

```php
protected convertUriToBinary(\Sabre\VObject\Component\VCard $output, \Sabre\VObject\Property\Uri $newProperty): \Sabre\VObject\Property\Binary|null
```

In vCard 4.0 attachments are encoded as data: uri. Even though these may
be valid in vCard 3.0 as well, we should convert those to BINARY if
possible, to improve compatibility.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$output` | **\Sabre\VObject\Component\VCard** |  |
| `$newProperty` | **\Sabre\VObject\Property\Uri** |  |





***

### convertParameters40

Adds parameters to a new property for vCard 4.0.

```php
protected convertParameters40(\Sabre\VObject\Property $newProperty, array $parameters): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$newProperty` | **\Sabre\VObject\Property** |  |
| `$parameters` | **array** |  |





***

### convertParameters30

Adds parameters to a new property for vCard 3.0.

```php
protected convertParameters30(\Sabre\VObject\Property $newProperty, array $parameters): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$newProperty` | **\Sabre\VObject\Property** |  |
| `$parameters` | **array** |  |





***


***
> Automatically generated on 2025-03-18
