***

# HtmlConverter

A helper class to convert HTML to Markdown.



* Full name: `\League\HTMLToMarkdown\HtmlConverter`
* This class implements:
[`\League\HTMLToMarkdown\HtmlConverterInterface`](./HtmlConverterInterface.md)

**See Also:**

* https://github.com/thephpleague/html-to-markdown/ - Latest version on GitHub.



## Properties


### environment



```php
protected \League\HTMLToMarkdown\Environment $environment
```






***

## Methods


### __construct

Constructor

```php
public __construct(\League\HTMLToMarkdown\Environment|array&lt;string,mixed&gt; $options = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **\League\HTMLToMarkdown\Environment&#124;array<string,mixed>** | Environment object or configuration options |





***

### getEnvironment



```php
public getEnvironment(): \League\HTMLToMarkdown\Environment
```












***

### getConfig



```php
public getConfig(): \League\HTMLToMarkdown\Configuration
```












***

### __invoke

Convert

```php
public __invoke(string $html): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string** |  |


**Return Value:**

The Markdown version of the html




**See Also:**

* \League\HTMLToMarkdown\HtmlConverter::convert - 

***

### convert

Convert

```php
public convert(string $html): string
```

Loads HTML and passes to getMarkdown()






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string** |  |


**Return Value:**

The Markdown version of the html



**Throws:**

- [`\InvalidArgumentException|\RuntimeException`](../../InvalidArgumentException|/RuntimeException.md)



***

### createDOMDocument



```php
private createDOMDocument(string $html): \DOMDocument
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string** |  |





***

### replaceMisplacedComments

Finds any comment nodes outside <html> element and moves them into <body>.

```php
private replaceMisplacedComments(\DOMDocument $document): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$document` | **\DOMDocument** |  |





**See Also:**

* https://github.com/thephpleague/html-to-markdown/issues/212 - * https://3v4l.org/7bC33 - 

***

### convertChildren

Convert Children

```php
private convertChildren(\League\HTMLToMarkdown\ElementInterface $element): void
```

Recursive function to drill into the DOM and convert each node into Markdown from the inside out.

Finds children of each node and convert those to #text nodes containing their Markdown equivalent,
starting with the innermost element and working up to the outermost element.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\League\HTMLToMarkdown\ElementInterface** |  |





***

### convertToMarkdown

Convert to Markdown

```php
protected convertToMarkdown(\League\HTMLToMarkdown\ElementInterface $element): string
```

Converts an individual node into a #text node containing a string of its Markdown equivalent.

Example: An <h3> node with text content of 'Title' becomes a text node with content of '### Title'






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\League\HTMLToMarkdown\ElementInterface** |  |


**Return Value:**

The converted HTML as Markdown




***

### sanitize



```php
protected sanitize(string $markdown): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$markdown` | **string** |  |





***

### setOptions

Pass a series of key-value pairs in an array; these will be passed
through the config and set.

```php
public setOptions(array&lt;string,mixed&gt; $options): $this
```

The advantage of this is that it can allow for static use (IE in Laravel).
An example being:

HtmlConverter::setOptions(['strip_tags' => true])->convert('<h1>test</h1>');






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **array<string,mixed>** |  |





***


***
> Automatically generated on 2025-03-15
