
# dba_pdo





* Full name: `\dba_pdo`
* Parent class: [`\dba_driver`](./dba_driver.md)



## Properties


### driver_dbtype



```php
public $driver_dbtype
```






***

## Methods


### connect



```php
public connect(mixed $server, mixed $scheme, mixed $port, mixed $user, mixed $pass, mixed $db, mixed $db_charset): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **mixed** | DB server name |
| `$scheme` | **mixed** | DB scheme |
| `$port` | **mixed** | DB port |
| `$user` | **mixed** | DB username |
| `$pass` | **mixed** | DB password |
| `$db` | **mixed** | database name |
| `$db_charset` | **mixed** |  |





**See Also:**

* \dba_driver::connect() - 

***

### q



```php
public q(mixed $sql): bool|array|\PDOStatement
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sql` | **mixed** | The SQL query to execute |


**Return Value:**


- \b false if not connected or PDOException occured on query
- \b array with results on a SELECT query
- \b PDOStatement on a non SELECT SQL query




**See Also:**

* \dba_driver::q() - 

***

### escape



```php
public escape(mixed $str): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **mixed** | The string to escape. |





***

### close



```php
public close(): mixed
```












***

### concat



```php
public concat(mixed $fld, mixed $sep): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fld` | **mixed** |  |
| `$sep` | **mixed** |  |





***

### use_index



```php
public use_index(mixed $str): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **mixed** |  |





***

### str_to_date



```php
public str_to_date(mixed $str): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **mixed** |  |





***

### quote_interval



```php
public quote_interval(mixed $txt): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$txt` | **mixed** |  |





***

### escapebin



```php
public escapebin(mixed $str): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **mixed** |  |





***

### unescapebin



```php
public unescapebin(mixed $str): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **mixed** |  |





***

### getdriver



```php
public getdriver(): mixed
```












***


## Inherited methods


### connect



```php
public connect(string $server, string $scheme, string $port, string $user, string $pass, string $db, mixed $db_charset): bool
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **string** | DB server name |
| `$scheme` | **string** | DB scheme |
| `$port` | **string** | DB port |
| `$user` | **string** | DB username |
| `$pass` | **string** | DB password |
| `$db` | **string** | database name |
| `$db_charset` | **mixed** |  |





***

### q



```php
public q(string $sql): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sql` | **string** | The SQL query to execute |





***

### escape



```php
public escape(string $str): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** | The string to escape. |





***

### close



```php
public close(): mixed
```




* This method is **abstract**.







***

### getdriver



```php
public getdriver(): mixed
```




* This method is **abstract**.







***

### __construct



```php
public __construct(mixed $server, mixed $scheme, mixed $port, mixed $user, mixed $pass, mixed $db, mixed $db_charset, mixed $install = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **mixed** |  |
| `$scheme` | **mixed** |  |
| `$port` | **mixed** |  |
| `$user` | **mixed** |  |
| `$pass` | **mixed** |  |
| `$db` | **mixed** |  |
| `$db_charset` | **mixed** |  |
| `$install` | **mixed** |  |





***

### get_null_date



```php
public get_null_date(): mixed
```












***

### get_install_script



```php
public get_install_script(): mixed
```












***

### get_table_quote



```php
public get_table_quote(): mixed
```












***

### utcnow



```php
public utcnow(): mixed
```












***

### install



```php
public install(mixed $server, mixed $scheme, mixed $port, mixed $user, mixed $pass, mixed $db): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **mixed** |  |
| `$scheme` | **mixed** |  |
| `$port` | **mixed** |  |
| `$user` | **mixed** |  |
| `$pass` | **mixed** |  |
| `$db` | **mixed** |  |





***

### dbg



```php
public dbg(int $dbg): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dbg` | **int** | 0 to disable debugging |





***

### __destruct



```php
public __destruct(): mixed
```












***

### quote_interval



```php
public quote_interval(mixed $txt): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$txt` | **mixed** |  |





***

### optimize_table



```php
public optimize_table(mixed $table): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$table` | **mixed** |  |





***

### concat



```php
public concat(mixed $fld, mixed $sep): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fld` | **mixed** |  |
| `$sep` | **mixed** |  |





***

### escapebin



```php
public escapebin(mixed $str): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **mixed** |  |





***

### unescapebin



```php
public unescapebin(mixed $str): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
