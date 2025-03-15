***

# UnitTestCase

Base class for our Unit Tests.

Base class for Hubzilla unit/integration tests. This extends the base
TestCase class from PHPUnit by connecting to a test database, and making the
database connection available to the code under test via the normal Hubzilla
mechanisms, i.e the \DBA::$dba global variable.

It also automatically loads database fixtures from yaml files in the
tests/unit/includes/dba/_files directory. And wraps each test run in it's
own database transaction.

* Full name: `\Zotlabs\Tests\Unit\UnitTestCase`
* Parent class: [`TestCase`](../../../PHPUnit/Framework/TestCase.md)



## Properties


### fixtures



```php
protected array $fixtures
```






***

### db_transaction



```php
protected ?\DbaTransaction $db_transaction
```






***

## Methods


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
