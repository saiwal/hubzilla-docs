***

# HTMLPurifier_Node

Abstract base node class that all others inherit from.

Why do we not use the DOM extension?  (1) It is not always available,
(2) it has funny constraints on the data it can represent,
whereas we want a maximally flexible representation, and (3) its
interface is a bit cumbersome.

* Full name: `\HTMLPurifier_Node`
* This class is an **Abstract class**



## Properties


### line

Line number of the start token in the source document

```php
public $line
```






***

### col

Column number of the start token in the source document. Null if unknown.

```php
public $col
```






***

### armor

Lookup array of processing that this token is exempt from.

```php
public $armor
```

Currently, valid values are "ValidateAttributes".




***

### dead

When true, this node should be ignored as non-existent.

```php
public $dead
```

Who is responsible for ignoring dead nodes?  FixNesting is
responsible for removing them before passing on to child
validators.




***

## Methods


### toTokenPair

Returns a pair of start and end tokens, where the end token
is null if it is not necessary. Does not include children.

```php
public toTokenPair(): mixed
```




* This method is **abstract**.







***


***
> Automatically generated on 2025-03-15
