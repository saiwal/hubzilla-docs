
# MarkdownTestHelper





* Full name: `\MarkdownTestHelper`




## Methods


### getInputOutputPaths

Takes an input directory containing .text and .(x)html files, and returns an array
of .text files and the corresponding output xhtml or html file. Can be used in a unit test data provider.

```php
public static getInputOutputPaths(string $directory): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$directory` | **string** | Input directory |





***

### assertSameNormalized

Applies PHPUnit's assertSame after normalizing both strings (e.g. ignoring whitespace differences).

```php
public static assertSameNormalized(string $string1, string $string2, string $message, bool $xhtml = true): mixed
```

Uses logic found originally in MDTest.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string1` | **string** |  |
| `$string2` | **string** |  |
| `$message` | **string** | Positive message to print when test fails (e.g. &quot;String1 matches String2&quot;) |
| `$xhtml` | **bool** |  |





***

### normalizeElementContent



```php
protected static normalizeElementContent(\DOMElement $element, bool $whitespace_preserve): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\DOMElement** | Modifies this element by reference |
| `$whitespace_preserve` | **bool** | Preserve Whitespace |





***

### normalizeElementAttributes



```php
protected static normalizeElementAttributes(\DOMElement $element): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\DOMElement** | Modifies this element by reference |





***


***
> Automatically generated on 2025-03-15
