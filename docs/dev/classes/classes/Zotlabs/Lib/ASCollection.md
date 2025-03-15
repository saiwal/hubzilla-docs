
# ASCollection

Class for dealing with fetching ActivityStreams collections (ordered or unordered, normal or paged).

Construct with either an existing object or url and an optional channel to sign requests.
$direction is 0 (default) to fetch from the beginning, and 1 to fetch from the end and reverse order the resultant array.
An optional limit to the number of records returned may also be specified.
Use $class->get() to return an array of collection members.

* Full name: `\Zotlabs\Lib\ASCollection`



## Properties


### channel



```php
private $channel
```






***

### nextpage



```php
private $nextpage
```






***

### limit



```php
private $limit
```






***

### direction



```php
private $direction
```






***

### data



```php
private $data
```






***

### history



```php
private $history
```






***

## Methods


### __construct



```php
public __construct(mixed $obj, mixed $channel = null, mixed $direction, mixed $limit): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$obj` | **mixed** |  |
| `$channel` | **mixed** |  |
| `$direction` | **mixed** |  |
| `$limit` | **mixed** |  |





***

### get



```php
public get(): mixed
```












***

### next



```php
public next(): mixed
```












***

### setnext



```php
public setnext(mixed $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
