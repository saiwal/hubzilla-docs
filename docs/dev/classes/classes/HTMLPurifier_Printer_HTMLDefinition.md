
# HTMLPurifier_Printer_HTMLDefinition





* Full name: `\HTMLPurifier_Printer_HTMLDefinition`
* Parent class: [`\HTMLPurifier_Printer`](./HTMLPurifier_Printer.md)



## Properties


### def



```php
protected $def
```






***

## Methods


### render



```php
public render(\HTMLPurifier_Config $config): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### renderDoctype

Renders the Doctype table

```php
protected renderDoctype(): string
```












***

### renderEnvironment

Renders environment table, which is miscellaneous info

```php
protected renderEnvironment(): string
```












***

### renderContentSets

Renders the Content Sets table

```php
protected renderContentSets(): string
```












***

### renderInfo

Renders the Elements ($info) table

```php
protected renderInfo(): string
```












***

### renderChildren

Renders a row describing the allowed children of an element

```php
protected renderChildren(\HTMLPurifier_ChildDef $def): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_ChildDef** | HTMLPurifier_ChildDef of pertinent element |





***

### listifyTagLookup

Listifies a tag lookup table.

```php
protected listifyTagLookup(array $array): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array` | **array** | Tag lookup array in form of array(&#039;tagname&#039; =&gt; true) |





***

### listifyObjectList

Listifies a list of objects by retrieving class names and internal state

```php
protected listifyObjectList(array $array): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array` | **array** | List of objects |





***

### listifyAttr

Listifies a hash of attributes to AttrDef classes

```php
protected listifyAttr(array $array): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array` | **array** | Array hash in form of array(&#039;attrname&#039; =&gt; HTMLPurifier_AttrDef) |





***

### heavyHeader

Creates a heavy header row

```php
protected heavyHeader(string $text, int $num = 1): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |
| `$num` | **int** |  |





***


## Inherited methods


### __construct

Initialize $generator.

```php
public __construct(): mixed
```












***

### prepareGenerator

Give generator necessary configuration if possible

```php
public prepareGenerator(\HTMLPurifier_Config $config): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$config` | **\HTMLPurifier_Config** |  |





***

### start

Returns a start tag

```php
protected start(string $tag, array $attr = array()): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **string** | Tag name |
| `$attr` | **array** | Attribute array |





***

### end

Returns an end tag

```php
protected end(string $tag): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **string** | Tag name |





***

### element

Prints a complete element with content inside

```php
protected element(string $tag, string $contents, array $attr = array(), bool $escape = true): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **string** | Tag name |
| `$contents` | **string** | Element contents |
| `$attr` | **array** | Tag attributes |
| `$escape` | **bool** | whether or not to escape contents |





***

### elementEmpty



```php
protected elementEmpty(string $tag, array $attr = array()): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **string** |  |
| `$attr` | **array** |  |





***

### text



```php
protected text(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### row

Prints a simple key/value row in a table.

```php
protected row(string $name, mixed $value): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Key |
| `$value` | **mixed** | Value |





***

### escape

Escapes a string for HTML output.

```php
protected escape(string $string): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | String to escape |





***

### listify

Takes a list of strings and turns them into a single list

```php
protected listify(string[] $array, bool $polite = false): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array` | **string[]** | List of strings |
| `$polite` | **bool** | Bool whether or not to add an end before the last |





***

### getClass

Retrieves the class of an object without prefixes, as well as metadata

```php
protected getClass(object $obj, string $sec_prefix = &#039;&#039;): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **object** | Object to determine class of |
| `$sec_prefix` | **string** | Further prefix to remove |





***


***
> Automatically generated on 2025-03-15
