
# SimplePie_Content_Type_Sniffer

Content-type sniffing



* Full name: `\SimplePie_Content_Type_Sniffer`
* Parent class: [`\SimplePie\Content\Type\Sniffer`](./SimplePie/Content/Type/Sniffer.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


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
> Automatically generated on 2025-03-18
