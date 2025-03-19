
# PermissionDescription

Encapsulates information the ACL dialog requires to describe
permission settings for an item with an empty ACL.

i.e the caption, icon, and tooltip for the no-ACL option in the ACL dialog.

* Full name: `\Zotlabs\Lib\PermissionDescription`



## Properties


### global_perm



```php
private $global_perm
```






***

### channel_perm



```php
private $channel_perm
```






***

### fallback_description



```php
private $fallback_description
```






***

## Methods


### fromDescription

If the interpretation of an empty ACL can't be summarised with a global default permission
or a specific permission setting then use this method and describe what it means instead.

```php
public static fromDescription(string $description): \Zotlabs\Lib\a
```

Remember to localize the description first.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$description` | **string** | - the localized caption for the no-ACL option in the ACL dialog. |


**Return Value:**

new instance of PermissionDescription




***

### fromStandalonePermission

Use this method only if the interpretation of an empty ACL doesn't fall back to a global
default permission. You should pass one of the constants from boot.php - PERMS_PUBLIC,
PERMS_NETWORK etc.

```php
public static fromStandalonePermission(int $perm): \Zotlabs\Lib\a
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$perm` | **int** | - a single enumerated constant permission - PERMS_PUBLIC, PERMS_NETWORK etc. |


**Return Value:**

new instance of PermissionDescription




***

### fromGlobalPermission

This is the preferred way to create a PermissionDescription, as it provides the most details.

```php
public static fromGlobalPermission(string $permname): \Zotlabs\Lib\a
```

Use this method if you know an empty ACL will result in one of the global default permissions
being used, such as channel_r_stream (for which you would pass 'view_stream').

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$permname` | **string** | - a key for the global perms array from get_perms() in permissions.php,<br />e.g. &#039;view_stream&#039;, &#039;view_profile&#039;, etc. |


**Return Value:**

new instance of PermissionDescription




***

### get_permission_description

Gets a localized description of the permission, or a generic message if the permission
is unknown.

```php
public get_permission_description(): string
```









**Return Value:**

description




***

### get_permission_icon

Returns an icon css class name if an appropriate one is available, e.g. "bi-globe" for Public,
otherwise returns empty string.

```php
public get_permission_icon(): string
```









**Return Value:**

icon css class name (often FontAwesome)




***

### get_permission_origin_description

Returns a localized description of where the permission came from, if this is known.

```php
public get_permission_origin_description(): string
```

If it's not know, or if the permission is standalone and didn't come from a default
permission setting, then empty string is returned.







**Return Value:**

description or empty string




***


***
> Automatically generated on 2025-03-19
