
# DBA





* Full name: `\DBA`



## Properties


### dba



```php
public static $dba
```



* This property is **static**.


***

### dbtype



```php
public static $dbtype
```



* This property is **static**.


***

### scheme



```php
public static $scheme
```



* This property is **static**.


***

### logging



```php
public static $logging
```



* This property is **static**.


***

### install_script



```php
public static $install_script
```



* This property is **static**.


***

### null_date



```php
public static $null_date
```



* This property is **static**.


***

### utc_now



```php
public static $utc_now
```



* This property is **static**.


***

### tquot



```php
public static $tquot
```



* This property is **static**.


***

## Methods


### dba_factory



```php
public static dba_factory(string $server, string $port, string $user, string $pass, string $db, string $dbtype, mixed $db_charset, bool $install = false): null|\dba_driver
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **string** | DB server name (or PDO dsn - e.g. mysqli:foobar.com;) |
| `$port` | **string** | DB port |
| `$user` | **string** | DB username |
| `$pass` | **string** | DB password |
| `$db` | **string** | database name |
| `$dbtype` | **string** | 0 for mysql, 1 for postgres |
| `$db_charset` | **mixed** |  |
| `$install` | **bool** | Defaults to false |


**Return Value:**

A database driver object (dba_pdo) or null if no driver found.




***


***
> Automatically generated on 2025-03-15
