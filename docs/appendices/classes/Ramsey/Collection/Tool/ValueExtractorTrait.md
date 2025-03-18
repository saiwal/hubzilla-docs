***

# ValueExtractorTrait

Provides functionality to extract the value of a property or method from an object.



* Full name: `\Ramsey\Collection\Tool\ValueExtractorTrait`




## Methods


### extractValue

Extracts the value of the given property or method from the object.

```php
protected extractValue(mixed $object, string $propertyOrMethod): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$object` | **mixed** | The object to extract the value from. |
| `$propertyOrMethod` | **string** | The property or method for which the<br />value should be extracted. |


**Return Value:**

the value extracted from the specified property or method.



**Throws:**
<p>if the method or property is not defined.</p>

- [`ValueExtractionException`](../Exception/ValueExtractionException.md)



***

***
> Automatically generated on 2025-03-18

