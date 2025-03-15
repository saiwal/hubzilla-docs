***

# SupportedPrivilegeSet

SupportedPrivilegeSet property.

This property encodes the {DAV:}supported-privilege-set property, as defined
in rfc3744. Please consult the rfc for details about it's structure.

This class expects a structure like the one given from
Sabre\DAVACL\Plugin::getSupportedPrivilegeSet as the argument in its
constructor.

* Full name: `\Sabre\DAVACL\Xml\Property\SupportedPrivilegeSet`
* This class implements:
[`\Sabre\Xml\XmlSerializable`](../../../Xml/XmlSerializable.md), [`\Sabre\DAV\Browser\HtmlOutput`](../../../DAV/Browser/HtmlOutput.md)



## Properties


### privileges

privileges.

```php
protected array $privileges
```






***

## Methods


### __construct

Constructor.

```php
public __construct(array $privileges): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$privileges` | **array** |  |





***

### getValue

Returns the privilege value.

```php
public getValue(): array
```












***

### xmlSerialize

The xmlSerialize method is called during xml writing.

```php
public xmlSerialize(\Sabre\Xml\Writer $writer): mixed
```

Use the $writer argument to write its own xml serialization.

An important note: do _not_ create a parent element. Any element
implementing XmlSerializable should only ever write what's considered
its 'inner xml'.

The parent of the current element is responsible for writing a
containing element.

This allows serializers to be re-used for different element names.

If you are opening new elements, you must also close them again.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$writer` | **\Sabre\Xml\Writer** |  |





***

### toHtml

Generate html representation for this value.

```php
public toHtml(\Sabre\DAV\Browser\HtmlOutputHelper $html): string
```

The html output is 100% trusted, and no effort is being made to sanitize
it. It's up to the implementor to sanitize user provided values.

The output must be in UTF-8.

The baseUri parameter is a url to the root of the application, and can
be used to construct local links.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **\Sabre\DAV\Browser\HtmlOutputHelper** |  |





***

### serializePriv

Serializes a property.

```php
private serializePriv(\Sabre\Xml\Writer $writer, string $privName, array $privilege): mixed
```

This is a recursive function.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$writer` | **\Sabre\Xml\Writer** |  |
| `$privName` | **string** |  |
| `$privilege` | **array** |  |





***


***
> Automatically generated on 2025-03-15
