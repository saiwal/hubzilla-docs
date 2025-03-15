
# Permutator

A Permutator iterates over all possible permutations of the given array
of elements.



* Full name: `\Permutator`



## Properties


### list

Constructs a new Permutator.

```php
public $list
```






***

### done



```php
public $done
```






***

### left



```php
public $left
```






***

## Methods


### __construct



```php
public __construct(mixed $list): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$list` | **mixed** |  |





***

### hasNext

Returns true if there is another permutation.

```php
public hasNext(): bool
```









**Return Value:**

true if there is another permutation, false if not.




***

### next

Gets the next permutation. Call hasNext() to ensure there is another one
first.

```php
public next(): array
```









**Return Value:**

the next permutation.




***


***
> Automatically generated on 2025-03-15
