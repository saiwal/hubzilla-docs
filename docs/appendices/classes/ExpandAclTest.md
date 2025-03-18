
# ExpandAclTest

TestCase for the expand_acl function



* Full name: `\ExpandAclTest`
* Parent class: [`PHPUnit_Framework_TestCase`](./PHPUnit_Framework_TestCase.md)




## Methods


### testExpandAclNormal

test expand_acl, perfect input

```php
public testExpandAclNormal(): mixed
```












***

### testExpandAclBigNumber

test with a big number

```php
public testExpandAclBigNumber(): mixed
```












***

### testExpandAclString

test with a string in it.

```php
public testExpandAclString(): mixed
```

TODO: is this valid input? Otherwise: should there be an exception?










***

### testExpandAclSpace

test with a ' ' in it.

```php
public testExpandAclSpace(): mixed
```

TODO: is this valid input? Otherwise: should there be an exception?










***

### testExpandAclEmpty

test empty input

```php
public testExpandAclEmpty(): mixed
```












***

### testExpandAclNoBrackets

test invalid input, no < at all

```php
public testExpandAclNoBrackets(): mixed
```

TODO: should there be an exception?










***

### testExpandAclJustOneBracket1

test invalid input, just open <

```php
public testExpandAclJustOneBracket1(): mixed
```

TODO: should there be an exception?










***

### testExpandAclJustOneBracket2

test invalid input, just close >

```php
public testExpandAclJustOneBracket2(): mixed
```

TODO: should there be an exception?










***

### testExpandAclCloseOnly

test invalid input, just close >

```php
public testExpandAclCloseOnly(): mixed
```

TODO: should there be an exception?










***

### testExpandAclOpenOnly

test invalid input, just open <

```php
public testExpandAclOpenOnly(): mixed
```

TODO: should there be an exception?










***

### testExpandAclNoMatching1

test invalid input, open and close do not match

```php
public testExpandAclNoMatching1(): mixed
```

TODO: should there be an exception?










***

### testExpandAclNoMatching2

test invalid input, open and close do not match

```php
public testExpandAclNoMatching2(): mixed
```

TODO: should there be an exception?










***

### testExpandAclEmptyMatch

test invalid input, empty <>

```php
public testExpandAclEmptyMatch(): mixed
```

TODO: should there be an exception? Or array(1, 3)
(This should be array(1,3) - mike)










***


***
> Automatically generated on 2025-03-18
