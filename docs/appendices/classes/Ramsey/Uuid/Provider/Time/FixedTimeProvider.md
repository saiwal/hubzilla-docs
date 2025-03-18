
# FixedTimeProvider

FixedTimeProvider uses a known time to provide the time

This provider allows the use of a previously-generated, or known, time
when generating time-based UUIDs.

* Full name: `\Ramsey\Uuid\Provider\Time\FixedTimeProvider`
* This class implements:
[`\Ramsey\Uuid\Provider\TimeProviderInterface`](../TimeProviderInterface.md)



## Properties


### time



```php
private \Ramsey\Uuid\Type\Time $time
```






***

## Methods


### __construct



```php
public __construct(\Ramsey\Uuid\Type\Time $time): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$time` | **\Ramsey\Uuid\Type\Time** |  |





***

### setUsec

Sets the `usec` component of the time

```php
public setUsec(int|string|\Ramsey\Uuid\Type\Integer $value): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **int&#124;string&#124;\Ramsey\Uuid\Type\Integer** | The `usec` value to set |





***

### setSec

Sets the `sec` component of the time

```php
public setSec(int|string|\Ramsey\Uuid\Type\Integer $value): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **int&#124;string&#124;\Ramsey\Uuid\Type\Integer** | The `sec` value to set |





***

### getTime

Returns a time object

```php
public getTime(): \Ramsey\Uuid\Type\Time
```












***


***
> Automatically generated on 2025-03-18
