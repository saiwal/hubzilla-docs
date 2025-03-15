***

# HtmlTools

From Epubli\Common\Tools - see https://github.com/epubli/common



* Full name: `\SebLucas\EPubMeta\Tools\HtmlTools`




## Methods


### convertEntitiesNamedToNumeric



```php
public static convertEntitiesNamedToNumeric(string $html): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string** |  |





***

### isBlockLevelElement



```php
public static isBlockLevelElement(string $name): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### truncate

performs a tag-aware truncation of (html-) strings, preserving tag integrity

```php
public static truncate(string[]|string $html, int|string $length = &quot;20%&quot;): bool|string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string[]&#124;string** |  |
| `$length` | **int&#124;string** |  |





***

### stripHtmlTags

strips all occurring html tags from $html (which can either be a string or an array of strings),
preserving all content enclosed by all tags in $keep and
dumping the content residing in all tags listed in $drop

```php
public static stripHtmlTags(string[]|string $html, string[] $keep = [&#039;title&#039;, &#039;br&#039;, &#039;p&#039;, &#039;h1&#039;, &#039;h2&#039;, &#039;h3&#039;, &#039;h4&#039;, &#039;h5&#039;, &#039;span&#039;, &#039;div&#039;, &#039;i&#039;, &#039;strong&#039;, &#039;b&#039;, &#039;table&#039;, &#039;td&#039;, &#039;th&#039;, &#039;tr&#039;], string[] $drop = [&#039;head&#039;, &#039;style&#039;]): string[]|string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **string[]&#124;string** |  |
| `$keep` | **string[]** |  |
| `$drop` | **string[]** |  |





***


***
> Automatically generated on 2025-03-15
