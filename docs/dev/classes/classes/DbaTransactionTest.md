***

# DbaTransactionTest

Test database transactions.

This class subclass the base PHPUnit TestCase class, since we do _not_
want a real database connection for these tests. We're testing functionality
of the database adapter itself, so we choose to stub the underlying db driver
to be able to assert that the adapter behaves as it should.

* Full name: `\DbaTransactionTest`
* Parent class: [`TestCase`](./PHPUnit/Framework/TestCase.md)



## Properties


### pdo_stub



```php
private $pdo_stub
```






***

## Methods


### setUp



```php
public setUp(): void
```












***

### test_transaction_initialized_on_construction

Test that creating a DbaTransaction object initiates a database transaction.

```php
public test_transaction_initialized_on_construction(): void
```












***

### test_uncommitted_transaction_is_rolled_back_on_destruction

Test that a transaction is rolled back when the DbaTransaction object
is destroyed.

```php
public test_uncommitted_transaction_is_rolled_back_on_destruction(): void
```












***

### test_committed_transaction_is_not_rolled_back

Test that a committed transaction is not rolled back when the
DbaTransaction object goes out of scope.

```php
public test_committed_transaction_is_not_rolled_back(): void
```












***

### test_that_committing_an_already_committed_transaction_does_nothing

Test that commiting a transaction more than once is a no-op.

```php
public test_that_committing_an_already_committed_transaction_does_nothing(): void
```












***

### test_that_nesting_a_transaction_does_not_create_a_new_transaction_in_db

Test simulating constructing a DbaTransaction object when a transaction
is already active.

```php
public test_that_nesting_a_transaction_does_not_create_a_new_transaction_in_db(): void
```

This should _not_ initiate an actual DB transaction, not call the rollBack
method on destruction.










***


***
> Automatically generated on 2025-03-15
