***

# Reader

iCalendar/vCard/jCal/jCard/xCal/xCard reader object.

This object provides a few (static) convenience methods to quickly access
the parsers.

* Full name: `\Sabre\VObject\Reader`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`OPTION_FORGIVING`|public| |1|
|`OPTION_IGNORE_INVALID_LINES`|public| |2|


## Methods


### read

Parses a vCard or iCalendar object, and returns the top component.

```php
public static read(string|resource $data, int $options, string $charset = &#039;UTF-8&#039;): \Sabre\VObject\Document
```

The options argument is a bitfield. Pass any of the OPTIONS constant to
alter the parsers' behaviour.

You can either supply a string, or a readable stream for input.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string&#124;resource** |  |
| `$options` | **int** |  |
| `$charset` | **string** |  |





***

### readJson

Parses a jCard or jCal object, and returns the top component.

```php
public static readJson(string|resource|array $data, int $options): \Sabre\VObject\Document
```

The options argument is a bitfield. Pass any of the OPTIONS constant to
alter the parsers' behaviour.

You can either a string, a readable stream, or an array for its input.
Specifying the array is useful if json_decode was already called on the
input.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string&#124;resource&#124;array** |  |
| `$options` | **int** |  |





***

### readXML

Parses a xCard or xCal object, and returns the top component.

```php
public static readXML(string|resource $data, int $options): \Sabre\VObject\Document
```

The options argument is a bitfield. Pass any of the OPTIONS constant to
alter the parsers' behaviour.

You can either supply a string, or a readable stream for input.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string&#124;resource** |  |
| `$options` | **int** |  |





***


***
> Automatically generated on 2025-03-15
