
# Smarty_Internal_Method_AppendByRef

Smarty Method AppendByRef

Smarty::appendByRef() method

* Full name: `\Smarty_Internal_Method_AppendByRef`




## Methods


### appendByRef

appends values to template variables by reference

```php
public static appendByRef(\Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty $data, string $tpl_var, mixed& $value, bool $merge = false): \Smarty_Internal_Data|\Smarty_Internal_Template|\Smarty
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **\Smarty_Internal_Data&#124;\Smarty_Internal_Template&#124;\Smarty** |  |
| `$tpl_var` | **string** | the template variable name |
| `$value` | **mixed** | the referenced value to append |
| `$merge` | **bool** | flag if array elements shall be merged |





**See Also:**

* https://www.smarty.net/docs/en/api.append.by.ref.tpl - 

***


***
> Automatically generated on 2025-03-15
