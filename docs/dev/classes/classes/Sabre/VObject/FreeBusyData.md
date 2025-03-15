
# FreeBusyData

FreeBusyData is a helper class that manages freebusy information.



* Full name: `\Sabre\VObject\FreeBusyData`



## Properties


### start

Start timestamp.

```php
protected int $start
```






***

### end

End timestamp.

```php
protected int $end
```






***

### data

A list of free-busy times.

```php
protected array $data
```






***

## Methods


### __construct



```php
public __construct(mixed $start, mixed $end): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$start` | **mixed** |  |
| `$end` | **mixed** |  |





***

### add

Adds free or busytime to the data.

```php
public add(int $start, int $end, string $type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$start` | **int** |  |
| `$end` | **int** |  |
| `$type` | **string** | FREE, BUSY, BUSY-UNAVAILABLE or BUSY-TENTATIVE |





***

### getData



```php
public getData(): mixed
```












***


***
> Automatically generated on 2025-03-15
