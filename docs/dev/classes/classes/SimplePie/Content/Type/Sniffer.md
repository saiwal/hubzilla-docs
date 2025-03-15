
# Sniffer

Content-type sniffing

Based on the rules in http://tools.ietf.org/html/draft-abarth-mime-sniff-06

This is used since we can't always trust Content-Type headers, and is based
upon the HTML5 parsing rules.


This class can be overloaded with {@see \SimplePie\SimplePie::set_content_type_sniffer_class()}

* Full name: `\SimplePie\Content\Type\Sniffer`



## Properties


### file

File object

```php
public \SimplePie\File $file
```






***

## Methods


### __construct

Create an instance of the class with the input file

```php
public __construct(\SimplePie\Content\Type\Sniffer $file): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **\SimplePie\Content\Type\Sniffer** | Input file |





***

### get_type

Get the Content-Type of the specified file

```php
public get_type(): string
```









**Return Value:**

Actual Content-Type




***

### text_or_binary

Sniff text or binary

```php
public text_or_binary(): string
```









**Return Value:**

Actual Content-Type




***

### unknown

Sniff unknown

```php
public unknown(): string
```









**Return Value:**

Actual Content-Type




***

### image

Sniff images

```php
public image(): string
```









**Return Value:**

Actual Content-Type




***

### feed_or_html

Sniff HTML

```php
public feed_or_html(): string
```









**Return Value:**

Actual Content-Type




***


***
> Automatically generated on 2025-03-15
