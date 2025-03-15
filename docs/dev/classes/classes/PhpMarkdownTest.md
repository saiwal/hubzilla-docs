
# PhpMarkdownTest





* Full name: `\PhpMarkdownTest`
* Parent class: [`TestCase`](./PHPUnit/Framework/TestCase.md)




## Methods


### dataProviderForPhpMarkdown

Returns all php-markdown.mdtest tests

```php
public dataProviderForPhpMarkdown(): array
```












***

### testTransformingOfPhpMarkdown

Runs php-markdown.mdtest against Markdown::defaultTransform

```php
public testTransformingOfPhpMarkdown(string $inputPath, string $htmlPath, bool $xhtml = false): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inputPath` | **string** | Input markdown path |
| `$htmlPath` | **string** | File path of expected transformed output (X)HTML |
| `$xhtml` | **bool** | True if XHTML. Otherwise, HTML is assumed. |





***

### dataProviderForPhpMarkdownExceptEmphasis

Returns all php-markdown.mdtest tests EXCEPT Emphasis test.

```php
public dataProviderForPhpMarkdownExceptEmphasis(): array
```












***

### testPhpMarkdownMdTestWithMarkdownExtra

Runs php-markdown.mdtest against MarkdownExtra::defaultTransform

```php
public testPhpMarkdownMdTestWithMarkdownExtra(mixed $inputPath, mixed $htmlPath, bool $xhtml = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inputPath` | **mixed** |  |
| `$htmlPath` | **mixed** |  |
| `$xhtml` | **bool** |  |





***

### dataProviderForMarkdownExtra



```php
public dataProviderForMarkdownExtra(): array
```












***

### testTransformingOfMarkdownExtra



```php
public testTransformingOfMarkdownExtra(string $inputPath, string $htmlPath, bool $xhtml = false): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inputPath` | **string** | Input markdown path |
| `$htmlPath` | **string** | File path of expected transformed output (X)HTML |
| `$xhtml` | **bool** | True if XHTML. Otherwise, HTML is assumed. |





***

### dataProviderForRegularMarkdown



```php
public dataProviderForRegularMarkdown(): array
```












***

### testTransformingOfRegularMarkdown



```php
public testTransformingOfRegularMarkdown(string $inputPath, string $htmlPath, bool $xhtml = false): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inputPath` | **string** | Input markdown path |
| `$htmlPath` | **string** | File path of expected transformed output (X)HTML |
| `$xhtml` | **bool** | True if XHTML. Otherwise, HTML is assumed. |





***

### testMarkdownMdTestWithMarkdownExtra

Runs markdown.mdtest against MarkdownExtra::defaultTransform

```php
public testMarkdownMdTestWithMarkdownExtra(mixed $inputPath, mixed $htmlPath, bool $xhtml = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inputPath` | **mixed** |  |
| `$htmlPath` | **mixed** |  |
| `$xhtml` | **bool** |  |





***


***
> Automatically generated on 2025-03-15
