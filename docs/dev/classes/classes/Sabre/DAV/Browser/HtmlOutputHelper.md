
# HtmlOutputHelper

This class provides a few utility functions for easily generating HTML for
the browser plugin.



* Full name: `\Sabre\DAV\Browser\HtmlOutputHelper`



## Properties


### baseUri

Link to the root of the application.

```php
protected string $baseUri
```






***

### namespaceMap

List of xml namespaces.

```php
protected array $namespaceMap
```






***

## Methods


### __construct

Creates the object.

```php
public __construct(string $baseUri, array $namespaceMap): mixed
```

baseUri must point to the root of the application. This will be used to
easily generate links.

The namespaceMap contains an array with the list of xml namespaces and
their prefixes. WebDAV uses a lot of XML with complex namespaces, so
that can be used to make output a lot shorter.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$baseUri` | **string** |  |
| `$namespaceMap` | **array** |  |





***

### fullUrl

Generates a 'full' url based on a relative one.

```php
public fullUrl(string $path): string
```

For relative urls, the base of the application is taken as the reference
url, not the 'current url of the current request'.

Absolute urls are left alone.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### h

Escape string for HTML output.

```php
public h(scalar $input): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **scalar** |  |





***

### link

Generates a full <a>-tag.

```php
public link(string $url, string $label = null): string
```

Url is automatically expanded. If label is not specified, we re-use the
url.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** |  |
| `$label` | **string** |  |





***

### xmlName

This method takes an xml element in clark-notation, and turns it into a
shortened version with a prefix, if it was a known namespace.

```php
public xmlName(string $element): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **string** |  |





***


***
> Automatically generated on 2025-03-15
