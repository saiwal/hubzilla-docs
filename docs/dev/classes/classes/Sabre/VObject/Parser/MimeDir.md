
# MimeDir

MimeDir parser.

This class parses iCalendar 2.0 and vCard 2.1, 3.0 and 4.0 files. This
parser will return one of the following two objects from the parse method:

Sabre\VObject\Component\VCalendar
Sabre\VObject\Component\VCard

* Full name: `\Sabre\VObject\Parser\MimeDir`
* Parent class: [`\Sabre\VObject\Parser\Parser`](./Parser.md)



## Properties


### input

The input stream.

```php
protected resource $input
```






***

### root

Root component.

```php
protected \Sabre\VObject\Component $root
```






***

### charset

By default all input will be assumed to be UTF-8.

```php
protected string $charset
```

However, both iCalendar and vCard might be encoded using different
character sets. The character set is usually set in the mime-type.

If this is the case, use setEncoding to specify that a different
encoding will be used. If this is set, the parser will automatically
convert all incoming data to UTF-8.




***

### SUPPORTED_CHARSETS

The list of character sets we support when decoding.

```php
protected static $SUPPORTED_CHARSETS
```

This would be a const expression but for now we need to support PHP 5.5

* This property is **static**.


***

### lineBuffer

We need to look ahead 1 line every time to see if we need to 'unfold'
the next line.

```php
protected string|null $lineBuffer
```

If that was not the case, we store it here.




***

### lineIndex

The real current line number.

```php
protected $lineIndex
```






***

### startLine

In the case of unfolded lines, this property holds the line number for
the start of the line.

```php
protected int $startLine
```






***

### rawLine

Contains a 'raw' representation of the current line.

```php
protected string $rawLine
```






***

## Methods


### parse

Parses an iCalendar or vCard file.

```php
public parse(string|resource|null $input = null, int $options): \Sabre\VObject\Document
```

Pass a stream or a string. If null is parsed, the existing buffer is
used.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **string&#124;resource&#124;null** |  |
| `$options` | **int** |  |





***

### setCharset

By default all input will be assumed to be UTF-8.

```php
public setCharset(string $charset): mixed
```

However, both iCalendar and vCard might be encoded using different
character sets. The character set is usually set in the mime-type.

If this is the case, use setEncoding to specify that a different
encoding will be used. If this is set, the parser will automatically
convert all incoming data to UTF-8.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$charset` | **string** |  |





***

### setInput

Sets the input buffer. Must be a string or stream.

```php
public setInput(resource|string $input): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **resource&#124;string** |  |





***

### parseDocument

Parses an entire document.

```php
protected parseDocument(): mixed
```












***

### parseLine

Parses a line, and if it hits a component, it will also attempt to parse
the entire component.

```php
protected parseLine(string $line): \Sabre\VObject\Node
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$line` | **string** | Unfolded line |





***

### readLine

Reads a single line from the buffer.

```php
protected readLine(): string
```

This method strips any newlines and also takes care of unfolding.









**Throws:**

- [`EofException`](../EofException.md)



***

### readProperty

Reads a property or component from a line.

```php
protected readProperty(mixed $line): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$line` | **mixed** |  |





***

### unescapeValue

Unescapes a property value.

```php
public static unescapeValue(string $input, string $delimiter = &#039;;&#039;): string|string[]
```

vCard 2.1 says:
  * Semi-colons must be escaped in some property values, specifically
    ADR, ORG and N.
  * Semi-colons must be escaped in parameter values, because semi-colons
    are also use to separate values.
  * No mention of escaping backslashes with another backslash.
  * newlines are not escaped either, instead QUOTED-PRINTABLE is used to
    span values over more than 1 line.

vCard 3.0 says:
  * (rfc2425) Backslashes, newlines (\n or \N) and comma's must be
    escaped, all time time.
  * Comma's are used for delimiters in multiple values
  * (rfc2426) Adds to to this that the semi-colon MUST also be escaped,
    as in some properties semi-colon is used for separators.
  * Properties using semi-colons: N, ADR, GEO, ORG
  * Both ADR and N's individual parts may be broken up further with a
    comma.
  * Properties using commas: NICKNAME, CATEGORIES

vCard 4.0 (rfc6350) says:
  * Commas must be escaped.
  * Semi-colons may be escaped, an unescaped semi-colon _may_ be a
    delimiter, depending on the property.
  * Backslashes must be escaped
  * Newlines must be escaped as either \N or \n.
  * Some compound properties may contain multiple parts themselves, so a
    comma within a semi-colon delimited property may also be unescaped
    to denote multiple parts _within_ the compound property.
  * Text-properties using semi-colons: N, ADR, ORG, CLIENTPIDMAP.
  * Text-properties using commas: NICKNAME, RELATED, CATEGORIES, PID.

Even though the spec says that commas must always be escaped, the
example for GEO in Section 6.5.2 seems to violate this.

iCalendar 2.0 (rfc5545) says:
  * Commas or semi-colons may be used as delimiters, depending on the
    property.
  * Commas, semi-colons, backslashes, newline (\N or \n) are always
    escaped, unless they are delimiters.
  * Colons shall not be escaped.
  * Commas can be considered the 'default delimiter' and is described as
    the delimiter in cases where the order of the multiple values is
    insignificant.
  * Semi-colons are described as the delimiter for 'structured values'.
    They are specifically used in Semi-colons are used as a delimiter in
    REQUEST-STATUS, RRULE, GEO and EXRULE. EXRULE is deprecated however.

Now for the parameters

If delimiter is not set (empty string) this method will just return a string.
If it's a comma or a semi-colon the string will be split on those
characters, and always return an array.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **string** |  |
| `$delimiter` | **string** |  |





***

### unescapeParam

Unescapes a parameter value.

```php
private unescapeParam(string $input): mixed
```

vCard 2.1:
  * Does not mention a mechanism for this. In addition, double quotes
    are never used to wrap values.
  * This means that parameters can simply not contain colons or
    semi-colons.

vCard 3.0 (rfc2425, rfc2426):
  * Parameters _may_ be surrounded by double quotes.
  * If this is not the case, semi-colon, colon and comma may simply not
    occur (the comma used for multiple parameter values though).
  * If it is surrounded by double-quotes, it may simply not contain
    double-quotes.
  * This means that a parameter can in no case encode double-quotes, or
    newlines.

vCard 4.0 (rfc6350)
  * Behavior seems to be identical to vCard 3.0

iCalendar 2.0 (rfc5545)
  * Behavior seems to be identical to vCard 3.0

Parameter escaping mechanism (rfc6868) :
  * This rfc describes a new way to escape parameter values.
  * New-line is encoded as ^n
  * ^ is encoded as ^^.
  * " is encoded as ^'






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **string** |  |





***

### extractQuotedPrintableValue

Gets the full quoted printable value.

```php
private extractQuotedPrintableValue(): string
```

We need a special method for this, because newlines have both a meaning
in vCards, and in QuotedPrintable.

This method does not do any decoding.










***


## Inherited methods


### __construct

Creates the parser.

```php
public __construct(mixed $input = null, int $options): mixed
```

Optionally, it's possible to parse the input stream here.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |
| `$options` | **int** | any parser options (OPTION constants) |





***

### parse

This method starts the parsing process.

```php
public parse(mixed $input = null, int $options): array
```

If the input was not supplied during construction, it's possible to pass
it here instead.

If either input or options are not supplied, the defaults will be used.


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |
| `$options` | **int** |  |





***

### setInput

Sets the input data.

```php
public setInput(mixed $input): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
