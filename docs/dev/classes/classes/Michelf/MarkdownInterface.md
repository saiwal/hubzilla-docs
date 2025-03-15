
# MarkdownInterface

Markdown Parser Interface



* Full name: `\Michelf\MarkdownInterface`



## Methods


### defaultTransform

Initialize the parser and return the result of its transform method.

```php
public static defaultTransform(string $text): string
```

This will work fine for derived classes too.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### transform

Main function. Performs some preprocessing on the input text
and pass it through the document gamut.

```php
public transform(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***


***
> Automatically generated on 2025-03-15
