
# VCard

The VCard component.

This component represents the BEGIN:VCARD and END:VCARD found in every
vcard.

* Full name: `\Sabre\VObject\Component\VCard`
* Parent class: [`\Sabre\VObject\Document`](../Document.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`DEFAULT_VERSION`|public| |self::VCARD21|

## Properties


### defaultName

The default name for this component.

```php
public static string $defaultName
```

This should be 'VCALENDAR' or 'VCARD'.

* This property is **static**.


***

### version

Caching the version number.

```php
private int $version
```






***

### componentMap

This is a list of components, and which classes they should map to.

```php
public static array $componentMap
```



* This property is **static**.


***

### valueMap

List of value-types, and which classes they map to.

```php
public static array $valueMap
```



* This property is **static**.


***

### propertyMap

List of properties, and which classes they map to.

```php
public static array $propertyMap
```



* This property is **static**.


***

## Methods


### getDocumentType

Returns the current document type.

```php
public getDocumentType(): int
```












***

### convert

Converts the document to a different vcard version.

```php
public convert(int $target): \Sabre\VObject\Component\VCard
```

Use one of the VCARD constants for the target. This method will return
a copy of the vcard in the new version.

At the moment the only supported conversion is from 3.0 to 4.0.

If input and output version are identical, a clone is returned.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$target` | **int** |  |





***

### validate

Validates the node for correctness.

```php
public validate(int $options): array
```

The following options are supported:
  Node::REPAIR - May attempt to automatically repair the problem.

This method returns an array with detected problems.
Every element has the following properties:

 * level - problem level.
 * message - A human-readable string describing the issue.
 * node - A reference to the problematic node.

The level means:
  1 - The issue was repaired (only happens if REPAIR was turned on)
  2 - An inconsequential issue
  3 - A severe issue.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **int** |  |





***

### getValidationRules

A simple list of validation rules.

```php
public getValidationRules(): mixed
```

This is simply a list of properties, and how many times they either
must or must not appear.

Possible values per property:
  * 0 - Must not appear.
  * 1 - Must appear exactly once.
  * + - Must appear at least once.
  * * - Can appear any number of times.
  * ? - May appear, but not more than once.










***

### preferred

Returns a preferred field.

```php
public preferred(mixed $propertyName): \Sabre\VObject\Property|null
```

VCards can indicate whether a field such as ADR, TEL or EMAIL is
preferred by specifying TYPE=PREF (vcard 2.1, 3) or PREF=x (vcard 4, x
being a number between 1 and 100).

If neither of those parameters are specified, the first is returned, if
a field with that name does not exist, null is returned.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propertyName` | **mixed** |  |





***

### getByType

Returns a property with a specific TYPE value (ADR, TEL, or EMAIL).

```php
public getByType(string $propertyName, string $type): \Sabre\VObject\Property|null
```

This function will return null if the property does not exist. If there are
multiple properties with the same TYPE value, only one will be returned.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propertyName` | **string** |  |
| `$type` | **string** |  |





***

### getDefaults

This method should return a list of default property values.

```php
protected getDefaults(): array
```












***

### jsonSerialize

This method returns an array, with the representation as it should be
encoded in json. This is used to create jCard or jCal documents.

```php
public jsonSerialize(): array
```












***

### xmlSerialize

This method serializes the data into XML. This is used to create xCard or
xCal documents.

```php
public xmlSerialize(\Sabre\Xml\Writer $writer): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$writer` | **\Sabre\Xml\Writer** | XML writer |





***

### getClassNameForPropertyName

Returns the default class for a property name.

```php
public getClassNameForPropertyName(string $propertyName): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propertyName` | **string** |  |





***


## Inherited methods


### serialize

Turns the object back into a serialized blob.

```php
public serialize(): string
```












***

### jsonSerialize

This method returns an array, with the representation as it should be
encoded in JSON. This is used to create jCard or jCal documents.

```php
public jsonSerialize(): array
```












***

### xmlSerialize

This method serializes the data into XML. This is used to create xCard or
xCal documents.

```php
public xmlSerialize(\Sabre\Xml\Writer $writer): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$writer` | **\Sabre\Xml\Writer** | XML writer |





***

### destroy

Call this method on a document if you're done using it.

```php
public destroy(): mixed
```

It's intended to remove all circular references, so PHP can easily clean
it up.










***

### getIterator

Returns the iterator for this object.

```php
public getIterator(): \Sabre\VObject\ElementList
```












***

### setIterator

Sets the overridden iterator.

```php
public setIterator(\Sabre\VObject\ElementList $iterator): mixed
```

Note that this is not actually part of the iterator interface






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$iterator` | **\Sabre\VObject\ElementList** |  |





***

### validate

Validates the node for correctness.

```php
public validate(int $options): array
```

The following options are supported:
  Node::REPAIR - May attempt to automatically repair the problem.
  Node::PROFILE_CARDDAV - Validate the vCard for CardDAV purposes.
  Node::PROFILE_CALDAV - Validate the iCalendar for CalDAV purposes.

This method returns an array with detected problems.
Every element has the following properties:

 * level - problem level.
 * message - A human-readable string describing the issue.
 * node - A reference to the problematic node.

The level means:
  1 - The issue was repaired (only happens if REPAIR was turned on).
  2 - A warning.
  3 - An error.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **int** |  |





***

### count

Returns the number of elements.

```php
public count(): int
```












***

### offsetExists

Checks if an item exists through ArrayAccess.

```php
public offsetExists(int $offset): bool
```

This method just forwards the request to the inner iterator






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **int** |  |





***

### offsetGet

Gets an item through ArrayAccess.

```php
public offsetGet(int $offset): mixed
```

This method just forwards the request to the inner iterator






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **int** |  |





***

### offsetSet

Sets an item through ArrayAccess.

```php
public offsetSet(int $offset, mixed $value): mixed
```

This method just forwards the request to the inner iterator






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **int** |  |
| `$value` | **mixed** |  |





***

### offsetUnset

Sets an item through ArrayAccess.

```php
public offsetUnset(int $offset): mixed
```

This method just forwards the request to the inner iterator






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **int** |  |





***

### __construct

Creates a new document.

```php
public __construct(): mixed
```

We're changing the default behavior slightly here. First, we don't want
to have to specify a name (we already know it), and we want to allow
children to be specified in the first argument.

But, the default behavior also works.

So the two sigs:

new Document(array $children = [], $defaults = true);
new Document(string $name, array $children = [], $defaults = true)










***

### add

Adds a new property or component, and returns the new item.

```php
public add(): \Sabre\VObject\Node
```

This method has 3 possible signatures:

add(Component $comp) // Adds a new component
add(Property $prop)  // Adds a new property
add($name, $value, array $parameters = []) // Adds a new property
add($name, array $children = []) // Adds a new component
by name.










***

### remove

This method removes a component or property from this component.

```php
public remove(string|\Sabre\VObject\Property|\Sabre\VObject\Component $item): mixed
```

You can either specify the item by name (like DTSTART), in which case
all properties/components with that name will be removed, or you can
pass an instance of a property or component, in which case only that
exact item will be removed.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **string&#124;\Sabre\VObject\Property&#124;\Sabre\VObject\Component** |  |





***

### children

Returns a flat list of all the properties and components in this
component.

```php
public children(): array
```












***

### getComponents

This method only returns a list of sub-components. Properties are
ignored.

```php
public getComponents(): array
```












***

### select

Returns an array with elements that match the specified name.

```php
public select(string $name): array
```

This function is also aware of MIME-Directory groups (as they appear in
vcards). This means that if a property is grouped as "HOME.EMAIL", it
will also be returned when searching for just "EMAIL". If you want to
search for a property in a specific group, you can select on the entire
string ("HOME.EMAIL"). If you want to search on a specific property that
has not been assigned a group, specify ".EMAIL".






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getDefaults

This method should return a list of default property values.

```php
protected getDefaults(): array
```












***

### __get

Using 'get' you will either get a property or component.

```php
public __get(string $name): \Sabre\VObject\Property|null
```

If there were no child-elements found with the specified name,
null is returned.

To use this, this may look something like this:

$event = $calendar->VEVENT;






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### __isset

This method checks if a sub-element with the specified name exists.

```php
public __isset(string $name): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### __set

Using the setter method you can add properties or subcomponents.

```php
public __set(string $name, mixed $value): mixed
```

You can either pass a Component, Property
object, or a string to automatically create a Property.

If the item already exists, it will be removed. If you want to add
a new item with the same name, always use the add() method.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **mixed** |  |





***

### __unset

Removes all properties and components within this component with the
specified name.

```php
public __unset(string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### __clone

This method is automatically called when the object is cloned.

```php
public __clone(): mixed
```

Specifically, this will ensure all child elements are also cloned.










***

### getValidationRules

A simple list of validation rules.

```php
public getValidationRules(): mixed
```

This is simply a list of properties, and how many times they either
must or must not appear.

Possible values per property:
  * 0 - Must not appear.
  * 1 - Must appear exactly once.
  * + - Must appear at least once.
  * * - Can appear any number of times.
  * ? - May appear, but not more than once.

It is also possible to specify defaults and severity levels for
violating the rule.

See the VEVENT implementation for getValidationRules for a more complex
example.










***

### getDocumentType

Returns the current document type.

```php
public getDocumentType(): int
```












***

### create

Creates a new component or property.

```php
public create(string $name): mixed
```

If it's a known component, we will automatically call createComponent.
otherwise, we'll assume it's a property and call createProperty instead.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### createComponent

Creates a new component.

```php
public createComponent(string $name, array $children = null, bool $defaults = true): \Sabre\VObject\Component
```

This method automatically searches for the correct component class, based
on its name.

You can specify the children either in key=>value syntax, in which case
properties will automatically be created, or you can just pass a list of
Component and Property object.

By default, a set of sensible values will be added to the component. For
an iCalendar object, this may be something like CALSCALE:GREGORIAN. To
ensure that this does not happen, set $defaults to false.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$children` | **array** |  |
| `$defaults` | **bool** |  |





***

### createProperty

Factory method for creating new properties.

```php
public createProperty(string $name, mixed $value = null, array $parameters = null, string $valueType = null, int $lineIndex = null, string $lineString = null): \Sabre\VObject\Property
```

This method automatically searches for the correct property class, based
on its name.

You can specify the parameters either in key=>value syntax, in which case
parameters will automatically be created, or you can just pass a list of
Parameter objects.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **mixed** |  |
| `$parameters` | **array** |  |
| `$valueType` | **string** | Force a specific valuetype, such as URI or TEXT |
| `$lineIndex` | **int** |  |
| `$lineString` | **string** |  |





***

### getClassNameForPropertyValue

This method returns a full class-name for a value parameter.

```php
public getClassNameForPropertyValue(string $valueParam): string|null
```

For instance, DTSTART may have VALUE=DATE. In that case we will look in
our valueMap table and return the appropriate class name.

This method returns null if we don't have a specialized class.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$valueParam` | **string** |  |





***

### getClassNameForPropertyName

Returns the default class for a property name.

```php
public getClassNameForPropertyName(string $propertyName): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propertyName` | **string** |  |





***


***
> Automatically generated on 2025-03-15
