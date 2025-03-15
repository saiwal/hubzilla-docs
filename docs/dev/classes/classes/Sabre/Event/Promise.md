
# Promise

An implementation of the Promise pattern.

A promise represents the result of an asynchronous operation.
At any given point a promise can be in one of three states:

1. Pending (the promise does not have a result yet).
2. Fulfilled (the asynchronous operation has completed with a result).
3. Rejected (the asynchronous operation has completed with an error).

To get a callback when the operation has finished, use the `then` method.

* Full name: `\Sabre\Event\Promise`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`PENDING`|public| |0|
|`FULFILLED`|public| |1|
|`REJECTED`|public| |2|

## Properties


### state

The current state of this promise.

```php
public int $state
```






***

### subscribers

A list of subscribers. Subscribers are the callbacks that want us to let
them know if the callback was fulfilled or rejected.

```php
protected array $subscribers
```






***

### value

The result of the promise.

```php
protected mixed $value
```

If the promise was fulfilled, this will be the result value. If the
promise was rejected, this property hold the rejection reason.




***

## Methods


### __construct

Creates the promise.

```php
public __construct(callable $executor = null): mixed
```

The passed argument is the executor. The executor is automatically
called with two arguments.

Each are callbacks that map to $this->fulfill and $this->reject.
Using the executor is optional.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$executor` | **callable** |  |





***

### then

This method allows you to specify the callback that will be called after
the promise has been fulfilled or rejected.

```php
public then(callable $onFulfilled = null, callable $onRejected = null): \Sabre\Event\Promise
```

Both arguments are optional.

This method returns a new promise, which can be used for chaining.
If either the onFulfilled or onRejected callback is called, you may
return a result from this callback.

If the result of this callback is yet another promise, the result of
_that_ promise will be used to set the result of the returned promise.

If either of the callbacks return any other value, the returned promise
is automatically fulfilled with that value.

If either of the callbacks throw an exception, the returned promise will
be rejected and the exception will be passed back.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$onFulfilled` | **callable** |  |
| `$onRejected` | **callable** |  |





***

### otherwise

Add a callback for when this promise is rejected.

```php
public otherwise(callable $onRejected): \Sabre\Event\Promise
```

Its usage is identical to then(). However, the otherwise() function is
preferred.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$onRejected` | **callable** |  |





***

### fulfill

Marks this promise as fulfilled and sets its return value.

```php
public fulfill(mixed $value = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **mixed** |  |





***

### reject

Marks this promise as rejected, and set its rejection reason.

```php
public reject(\Throwable $reason): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reason` | **\Throwable** |  |





***

### wait

Stops execution until this promise is resolved.

```php
public wait(): mixed
```

This method stops execution completely. If the promise is successful with
a value, this method will return this value. If the promise was
rejected, this method will throw an exception.

This effectively turns the asynchronous operation into a synchronous
one. In PHP it might be useful to call this on the last promise in a
chain.










***

### invokeCallback

This method is used to call either an onFulfilled or onRejected callback.

```php
private invokeCallback(\Sabre\Event\Promise $subPromise, callable $callBack = null): mixed
```

This method makes sure that the result of these callbacks are handled
correctly, and any chained promises are also correctly fulfilled or
rejected.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$subPromise` | **\Sabre\Event\Promise** |  |
| `$callBack` | **callable** |  |





***


***
> Automatically generated on 2025-03-15
