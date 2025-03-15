***

# HtmlOutput

WebDAV properties that implement this interface are able to generate their
own html output for the browser plugin.

This is only useful for display purposes, and might make it a bit easier for
people to read and understand the value of some properties.

* Full name: `\Sabre\DAV\Browser\HtmlOutput`



## Methods


### toHtml

Generate html representation for this value.

```php
public toHtml(\Sabre\DAV\Browser\HtmlOutputHelper $html): string
```

The html output is 100% trusted, and no effort is being made to sanitize
it. It's up to the implementor to sanitize user provided values.

The output must be in UTF-8.

The baseUri parameter is a url to the root of the application, and can
be used to construct local links.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$html` | **\Sabre\DAV\Browser\HtmlOutputHelper** |  |





***


***
> Automatically generated on 2025-03-15
