
# Smarty_Internal_Method_LoadPlugin

Smarty Extension Loadplugin

$smarty->loadPlugin() method

* Full name: `\Smarty_Internal_Method_LoadPlugin`



## Properties


### plugin_files

Cache of searched plugin files

```php
public array $plugin_files
```






***

## Methods


### loadPlugin

Takes unknown classes and loads plugin files for them
class name format: Smarty_PluginType_PluginName
plugin filename format: plugintype.pluginname.php

```php
public loadPlugin(\Smarty $smarty, string $plugin_name, bool $check): bool|string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$smarty` | **\Smarty** |  |
| `$plugin_name` | **string** | class plugin name to load |
| `$check` | **bool** | check if already loaded |




**Throws:**

- [`SmartyException`](./SmartyException.md)



***


***
> Automatically generated on 2025-03-18
