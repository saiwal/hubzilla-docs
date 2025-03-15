***

# Writer

iCalendar/vCard/jCal/jCard/xCal/xCard writer object.

This object provides a few (static) convenience methods to quickly access
the serializers.

* Full name: `\Sabre\VObject\Writer`




## Methods


### write

Serializes a vCard or iCalendar object.

```php
public static write(\Sabre\VObject\Component $component): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$component` | **\Sabre\VObject\Component** |  |





***

### writeJson

Serializes a jCal or jCard object.

```php
public static writeJson(\Sabre\VObject\Component $component, int $options): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$component` | **\Sabre\VObject\Component** |  |
| `$options` | **int** |  |





***

### writeXml

Serializes a xCal or xCard object.

```php
public static writeXml(\Sabre\VObject\Component $component): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$component` | **\Sabre\VObject\Component** |  |





***


***
> Automatically generated on 2025-03-15
