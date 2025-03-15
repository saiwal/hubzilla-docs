***

# HTMLPurifier_Zipper

A zipper is a purely-functional data structure which contains
a focus that can be efficiently manipulated.  It is known as
a "one-hole context".  This mutable variant implements a zipper
for a list as a pair of two arrays, laid out as follows:

Base list: 1 2 3 4 [ ] 6 7 8 9
     Front list: 1 2 3 4
     Back list: 9 8 7 6

User is expected to keep track of the "current element" and properly
fill it back in as necessary.  (ToDo: Maybe it's more user friendly
to implicitly track the current element?)

Nota bene: the current class gets confused if you try to store NULLs
in the list.

* Full name: `\HTMLPurifier_Zipper`



## Properties


### front



```php
public $front
```






***

### back



```php
public $back
```






***

## Methods


### __construct



```php
public __construct(mixed $front, mixed $back): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$front` | **mixed** |  |
| `$back` | **mixed** |  |





***

### fromArray

Creates a zipper from an array, with a hole in the
0-index position.

```php
public static fromArray(mixed $array): \Tuple
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array` | **mixed** |  |


**Return Value:**

of zipper and element of first position.




***

### toArray

Convert zipper back into a normal array, optionally filling in
the hole with a value. (Usually you should supply a $t, unless you
are at the end of the array.)

```php
public toArray(mixed $t = NULL): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$t` | **mixed** |  |





***

### next

Move hole to the next element.

```php
public next(mixed $t): \Original
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$t` | **mixed** | Element to fill hole with |


**Return Value:**

contents of new hole.




***

### advance

Iterated hole advancement.

```php
public advance(mixed $t, mixed $n): \Original
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$t` | **mixed** | Element to fill hole with |
| `$n` | **mixed** |  |


**Return Value:**

contents of new hole, i away




***

### prev

Move hole to the previous element

```php
public prev(mixed $t): \Original
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$t` | **mixed** | Element to fill hole with |


**Return Value:**

contents of new hole.




***

### delete

Delete contents of current hole, shifting hole to
next element.

```php
public delete(): \Original
```









**Return Value:**

contents of new hole.




***

### done

Returns true if we are at the end of the list.

```php
public done(): bool
```












***

### insertBefore

Insert element before hole.

```php
public insertBefore(mixed $t): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$t` | **mixed** |  |





***

### insertAfter

Insert element after hole.

```php
public insertAfter(mixed $t): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$t` | **mixed** |  |





***

### splice

Splice in multiple elements at hole.  Functional specification
in terms of array_splice:

```php
public splice(mixed $t, mixed $delete, mixed $replacement): mixed
```

$arr1 = $arr;
     $old1 = array_splice($arr1, $i, $delete, $replacement);

     list($z, $t) = HTMLPurifier_Zipper::fromArray($arr);
     $t = $z->advance($t, $i);
     list($old2, $t) = $z->splice($t, $delete, $replacement);
     $arr2 = $z->toArray($t);

     assert($old1 === $old2);
     assert($arr1 === $arr2);

NB: the absolute index location after this operation is
*unchanged!*






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$t` | **mixed** |  |
| `$delete` | **mixed** |  |
| `$replacement` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
