***

# AdminAccountsTest

Base class for writing module tests.

This test class adds a number of helper methods to the base from
the UnitTestCase class, useful when testing Modules (Controllers)
that handle incoming requests.

* Full name: `\Zotlabs\Tests\Unit\Module\AdminAccountsTest`
* Parent class: [`\Zotlabs\Tests\Unit\Module\TestCase`](./TestCase.md)



## Properties


### stub_check_security



```php
protected $stub_check_security
```






***

### stub_is_site_admin



```php
protected $stub_is_site_admin
```






***

### stub_goaway



```php
protected $stub_goaway
```






***

### stub_notice



```php
protected $stub_notice
```






***

### notice



```php
protected array $notice
```






***

## Methods


### setup_stubs

Set up the stubs common for the tests.

```php
public setup_stubs(): void
```












***

### test_blocking_accounts_marks_selected_accounts_as_blocked



```php
public test_blocking_accounts_marks_selected_accounts_as_blocked(): void
```












***

### test_unblocking_accounts_clears_the_blocked_flag



```php
public test_unblocking_accounts_clears_the_blocked_flag(): void
```












***

### test_deleting_accouns_remove_them_from_db



```php
public test_deleting_accouns_remove_them_from_db(): void
```












***

### test_approving_pending_accounts_clears_pending_flag



```php
public test_approving_pending_accounts_clears_pending_flag(): void
```












***

### stub_check_form_security

Stub the check_form_security_token_ForbiddenOnErr.

```php
protected stub_check_form_security(): void
```












***

### stub_is_site_admin

Stub the call to is_site_admin in the Admin main module.

```php
protected stub_is_site_admin(): void
```












***

### stub_goaway

Stub the goaway function.

```php
protected stub_goaway(): void
```

Will throw an RedirectException with the URL being redirected to
as the exception message.









**Throws:**

- [`RedirectException`](./RedirectException.md)



***

### stub_notice



```php
protected stub_notice(): void
```












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

### cleanup_stubs



```php
public cleanup_stubs(): void
```












***

### do_request



```php
protected do_request(string $method, string $uri, array $query = [], array $params = []): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$method` | **string** |  |
| `$uri` | **string** |  |
| `$query` | **array** |  |
| `$params` | **array** |  |





***

### get

Emulate a GET request.

```php
protected get(string $uri, array $query = []): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** | The URI to request. Typically this will be the module<br />name, followed by any req args separated by slashes. |
| `$query` | **array** | Assciative array of query args, with the parameters<br />as keys. |





***

### post

Emulate a POST request.

```php
protected post(string $uri, array $query = [], array $params = []): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** | The URI to request. Typically this will be the module<br />name, followed by any req args separated by slashes. |
| `$query` | **array** | Associative array of query args, with the parameters<br />as keys. |
| `$params` | **array** | Associative array of POST params, with the param names<br />as keys. |





***

### assertPageContains

Helper to simplify asserting contents in the rendered page.

```php
protected assertPageContains(string $needle): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$needle` | **string** | The expected string to find. |





***

### stub_killme

Stub out the `killme` function.

```php
protected stub_killme(): void
```

Useful for testing modules that call this function directly.

Instead of calling exit, the stub will throw a `KillmeException`,
that can be caught by the test code to regain control after request
processing is terminated.

**Example:**

    public function test_something(): void {
        $this->stub_killme();

        try {
            killme();
        } catch (KillmeException $e) {
            $this->assertSomething(...);
        }
    }

It's also possible to use the builting PHPUnit expecations to verify
that the function was called.

    public function test_something(): void {
        $this->stub_killme();
        $this->expectException(KillmeException::class);

        killme();
    }

This is useful if you only want to check that processing was terminated
with the `killme()` function.









**Throws:**

- [`KillmeException`](./KillmeException.md)



***

### stub_goaway

Stub out the `goaway` function.

```php
protected stub_goaway(): void
```

Useful for testing modules that calls this function directly.

Instead of calling `killme()`, the stub will throw a RedirectException
with the target URL as the exception message. This allows the test code
to regain control after request processing is terminated.

**Example:**

    public function test_redirect(): void {
        $this->stub_goaway();

        try {
            goaway('https://example.com/some_uri');
        } catch (RedirectException $e) {
            $this->assertEquals('https://example.com/some_uri', $e->getMessage());
            $this->assertSomethingElse(...);
        }
    }
It's also possible to use the builting PHPUnit expecations to verify
that the function was called.

    public function test_something(): void {
        $this->stub_goaway();
        $this->expectException(RedirectException::class);
        $this->expectExceptionMessage('https://example.com/some_uri');

        goaway('https://example.com/some_uri');
    }

This is useful if you only want to check that the request was redirected.









**Throws:**

- [`RedirectException`](./RedirectException.md)



***

### expectRedirectTo

Shorthand function to expect a redirect to a given URL.

```php
protected expectRedirectTo(string $destination): void
```

**Example:**

public function test_redirect(): void {
    $this->expectRedirectTo('https://example.com/some_uri');
    goaway('https://example.com/some_uri');
}






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$destination` | **string** |  |





***


***
> Automatically generated on 2025-03-15
