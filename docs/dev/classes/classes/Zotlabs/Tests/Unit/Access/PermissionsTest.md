
# PermissionsTest

Base class for our Unit Tests.



* Full name: `\Zotlabs\Tests\Unit\Access\PermissionsTest`
* Parent class: [`\Zotlabs\Tests\Unit\UnitTestCase`](../UnitTestCase.md)




## Methods


### testVersion



```php
public testVersion(): mixed
```












***

### testVersionEqualsPermissionRoles



```php
public testVersionEqualsPermissionRoles(): mixed
```












***

### testPerms



```php
public testPerms(): mixed
```












***

### testPermsFilter

filter parmeter is only used in hook \b permissions_list. So the result
in this test should be the same as if there was no filter parameter.

```php
public testPermsFilter(): mixed
```












***

### testFilledPerms

Better should mock Permissions::Perms, but not possible with static methods.

```php
public testFilledPerms(array $permarr, array $expected): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$permarr` | **array** | An indexed permissions array to pass |
| `$expected` | **array** | The expected result perms array |





***

### FilledPermsProvider



```php
public static FilledPermsProvider(): array
```



* This method is **static**.





**Return Value:**

An associative array with test values for FilledPerms()
* \e array Indexed array which is passed as parameter to FilledPerms()
* \e array Expected associative result array with filled perms




***

### testFilledPermsNull



```php
public testFilledPermsNull(): mixed
```












***

### testOPerms



```php
public testOPerms(array $permarr, array $expected): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$permarr` | **array** | The params to pass to the OPerms method |
| `$expected` | **array** | The expected result |





***

### OPermsProvider



```php
public static OPermsProvider(): array
```



* This method is **static**.





**Return Value:**

An associative array with test values for OPerms()
* \e array Array with perms to test
* \e array Expected result array




***

### testPermsCompare



```php
public testPermsCompare(array $p1, array $p2, bool $expectedresult): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$p1` | **array** | The first permission |
| `$p2` | **array** | The second permission |
| `$expectedresult` | **bool** | The expected result of the tested method |





***

### permsCompareProvider



```php
public static permsCompareProvider(): array
```



* This method is **static**.





**Return Value:**

An associative array with test values for PermsCompare()
* \e array 1st array with perms
* \e array 2nd array with perms
* \e boolean expected result for the perms comparison




***


## Inherited methods


### setup_test_db

Connect to the test db, load fixtures and global config.

```php
protected setup_test_db(): void
```

This function is executed before every test.

The transaction is rolled back in the `cleanup_test_db()` function
that's executed after every test.










***

### init_app

Initialize the global App properties.

```php
protected init_app(): void
```












***

### cleanup_test_db

Roll back test database to it's original state, cleaning up
any changes from the test.

```php
protected cleanup_test_db(): void
```

This function is executes after evert tests.










***

### connect_to_test_db

Connect to the test database,

```php
protected connect_to_test_db(): void
```

By default it will connect to a MySQL database with the following settings:

  - HZ_TEST_DB_HOST: db
  - HZ_TEST_DB_PORT: default
  - HZ_TEST_DB_USER: test_user
  - HZ_TEST_DB_PASS: hubzilla
  - HZ_TEST_DB_DATABASE: hubzilla_test_db
  - HZ_TEST_DB_TYPE: mysql (can also be "postgres")
  - HZ_TEST_DB_CHARSET: UTF8

All of these settings can be overridden by the test runner by setting ENV vars
named as above with the values you want to override.










***

### dbtype

Return the database type from a string.

```php
private static dbtype(string $type): \Zotlabs\Tests\Unit\The
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string** | The database type, can be either mysql or postgres. |


**Return Value:**

database type constant matching the passed in type, or DBTYPE_MYSQL
if $type is empty or invalid.




***

### loadFixtures

Load database fixtures from the fixture path.

```php
private loadFixtures(): void
```












***

### loadFixture

Load database fixtures from a specific file.

```php
private loadFixture(string $file): void
```

The file must be a yaml file named the same as the table in the database
it should populate.

The file also need to have a root key with the same name as the table.
Under which it contains an array of rows that should be inserted into
the db table.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** | The path and filename of the fixture to load.<br />The path name is relative to the current working<br />directory of the process, which should normally<br />be the Hubzilla root directory. |





***


***
> Automatically generated on 2025-03-15
