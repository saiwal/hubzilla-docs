***

# Smarty_Internal_Runtime_FilterHandler

Class for filter processing



* Full name: `\Smarty_Internal_Runtime_FilterHandler`




## Methods


### runFilter

Run filters over content
The filters will be lazy loaded if required
class name format: Smarty_FilterType_FilterName
plugin filename format: filtertype.filtername.php
Smarty2 filter plugins could be used

```php
public runFilter(string $type, string $content, \Smarty_Internal_Template $template): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | the type of filter (&#039;pre&#039;,&#039;post&#039;,&#039;output&#039;) which shall run |
| `$content` | **string** | the content which shall be processed by the filters |
| `$template` | **\Smarty_Internal_Template** | template object |


**Return Value:**

the filtered content



**Throws:**

- [`SmartyException`](./SmartyException.md)



***


***
> Automatically generated on 2025-03-15
