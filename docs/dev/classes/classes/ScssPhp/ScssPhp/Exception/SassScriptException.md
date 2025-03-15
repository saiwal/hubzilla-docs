***

# SassScriptException

An exception thrown by SassScript.

This class does not implement SassException on purpose, as it should
never be returned to the outside code. The compilation will catch it
and replace it with a SassException reporting the location of the
error.

* Full name: `\ScssPhp\ScssPhp\Exception\SassScriptException`
* Parent class: [`Exception`](../../../Exception.md)




## Methods


### forArgument

Creates a SassScriptException with support for an argument name.

```php
public static forArgument(string $message, string|null $name = null): \ScssPhp\ScssPhp\Exception\SassScriptException
```

This helper ensures a consistent handling of argument names in the
error message, without duplicating it.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **string** |  |
| `$name` | **string&#124;null** | The argument name, without $ |





***


***
> Automatically generated on 2025-03-15
