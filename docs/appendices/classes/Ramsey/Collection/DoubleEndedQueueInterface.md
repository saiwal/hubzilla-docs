
# DoubleEndedQueueInterface

A linear collection that supports element insertion and removal at both ends.

Most `DoubleEndedQueueInterface` implementations place no fixed limits on the
number of elements they may contain, but this interface supports
capacity-restricted double-ended queues as well as those with no fixed size
limit.

This interface defines methods to access the elements at both ends of the
double-ended queue. Methods are provided to insert, remove, and examine the
element. Each of these methods exists in two forms: one throws an exception
if the operation fails, the other returns a special value (either `null` or
`false`, depending on the operation). The latter form of the insert operation
is designed specifically for use with capacity-restricted implementations; in
most implementations, insert operations cannot fail.

The twelve methods described above are summarized in the following table:

<table>
<caption>Summary of DoubleEndedQueueInterface methods</caption>
<thead>
<tr>
<th></th>
<th colspan=2>First Element (Head)</th>
<th colspan=2>Last Element (Tail)</th>
</tr>
<tr>
<td></td>
<td><em>Throws exception</em></td>
<td><em>Special value</em></td>
<td><em>Throws exception</em></td>
<td><em>Special value</em></td>
</tr>
</thead>
<tbody>
<tr>
<th>Insert</th>
<td><code>addFirst()</code></td>
<td><code>offerFirst()</code></td>
<td><code>addLast()</code></td>
<td><code>offerLast()</code></td>
</tr>
<tr>
<th>Remove</th>
<td><code>removeFirst()</code></td>
<td><code>pollFirst()</code></td>
<td><code>removeLast()</code></td>
<td><code>pollLast()</code></td>
</tr>
<tr>
<th>Examine</th>
<td><code>firstElement()</code></td>
<td><code>peekFirst()</code></td>
<td><code>lastElement()</code></td>
<td><code>peekLast()</code></td>
</tr>
</tbody>
</table>

This interface extends the `QueueInterface`. When a double-ended queue is
used as a queue, FIFO (first-in-first-out) behavior results. Elements are
added at the end of the double-ended queue and removed from the beginning.
The methods inherited from the `QueueInterface` are precisely equivalent to
`DoubleEndedQueueInterface` methods as indicated in the following table:

<table>
<caption>Comparison of QueueInterface and DoubleEndedQueueInterface methods</caption>
<thead>
<tr>
<th>QueueInterface Method</th>
<th>DoubleEndedQueueInterface Method</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>add()</code></td>
<td><code>addLast()</code></td>
</tr>
<tr>
<td><code>offer()</code></td>
<td><code>offerLast()</code></td>
</tr>
<tr>
<td><code>remove()</code></td>
<td><code>removeFirst()</code></td>
</tr>
<tr>
<td><code>poll()</code></td>
<td><code>pollFirst()</code></td>
</tr>
<tr>
<td><code>element()</code></td>
<td><code>firstElement()</code></td>
</tr>
<tr>
<td><code>peek()</code></td>
<td><code>peekFirst()</code></td>
</tr>
</tbody>
</table>

Double-ended queues can also be used as LIFO (last-in-first-out) stacks. When
a double-ended queue is used as a stack, elements are pushed and popped from
the beginning of the double-ended queue. Stack concepts are precisely
equivalent to `DoubleEndedQueueInterface` methods as indicated in the table
below:

<table>
<caption>Comparison of stack concepts and DoubleEndedQueueInterface methods</caption>
<thead>
<tr>
<th>Stack concept</th>
<th>DoubleEndedQueueInterface Method</th>
</tr>
</thead>
<tbody>
<tr>
<td><em>push</em></td>
<td><code>addFirst()</code></td>
</tr>
<tr>
<td><em>pop</em></td>
<td><code>removeFirst()</code></td>
</tr>
<tr>
<td><em>peek</em></td>
<td><code>peekFirst()</code></td>
</tr>
</tbody>
</table>

Note that the `peek()` method works equally well when a double-ended queue is
used as a queue or a stack; in either case, elements are drawn from the
beginning of the double-ended queue.

While `DoubleEndedQueueInterface` implementations are not strictly required
to prohibit the insertion of `null` elements, they are strongly encouraged to
do so. Users of any `DoubleEndedQueueInterface` implementations that do allow
`null` elements are strongly encouraged *not* to take advantage of the
ability to insert nulls. This is so because `null` is used as a special
return value by various methods to indicated that the double-ended queue is
empty.

* Full name: `\Ramsey\Collection\DoubleEndedQueueInterface`
* Parent interfaces: [`\Ramsey\Collection\QueueInterface`](./QueueInterface.md)


## Methods


### addFirst

Inserts the specified element at the front of this queue if it is
possible to do so immediately without violating capacity restrictions.

```php
public addFirst(\Ramsey\Collection\T $element): bool
```

When using a capacity-restricted double-ended queue, it is generally
preferable to use the `offerFirst()` method.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\Ramsey\Collection\T** | The element to add to the front of this queue. |


**Return Value:**

`true` if this queue changed as a result of the call.



**Throws:**
<p>if a queue refuses to add a particular element
for any reason other than that it already contains the element.
Implementations should use a more-specific exception that extends
<code class="prettyprint">\RuntimeException</code>.</p>

- [`RuntimeException`](../../RuntimeException.md)



***

### addLast

Inserts the specified element at the end of this queue if it is possible
to do so immediately without violating capacity restrictions.

```php
public addLast(\Ramsey\Collection\T $element): bool
```

When using a capacity-restricted double-ended queue, it is generally
preferable to use the `offerLast()` method.

This method is equivalent to `add()`.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\Ramsey\Collection\T** | The element to add to the end of this queue. |


**Return Value:**

`true` if this queue changed as a result of the call.



**Throws:**
<p>if a queue refuses to add a particular element
for any reason other than that it already contains the element.
Implementations should use a more-specific exception that extends
<code class="prettyprint">\RuntimeException</code>.</p>

- [`RuntimeException`](../../RuntimeException.md)



***

### offerFirst

Inserts the specified element at the front of this queue if it is
possible to do so immediately without violating capacity restrictions.

```php
public offerFirst(\Ramsey\Collection\T $element): bool
```

When using a capacity-restricted queue, this method is generally
preferable to `addFirst()`, which can fail to insert an element only by
throwing an exception.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\Ramsey\Collection\T** | The element to add to the front of this queue. |


**Return Value:**

`true` if the element was added to this queue, else `false`.




***

### offerLast

Inserts the specified element at the end of this queue if it is possible
to do so immediately without violating capacity restrictions.

```php
public offerLast(\Ramsey\Collection\T $element): bool
```

When using a capacity-restricted queue, this method is generally
preferable to `addLast()` which can fail to insert an element only by
throwing an exception.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\Ramsey\Collection\T** | The element to add to the end of this queue. |


**Return Value:**

`true` if the element was added to this queue, else `false`.




***

### removeFirst

Retrieves and removes the head of this queue.

```php
public removeFirst(): \Ramsey\Collection\T
```

This method differs from `pollFirst()` only in that it throws an
exception if this queue is empty.







**Return Value:**

the first element in this queue.



**Throws:**
<p>if this queue is empty.</p>

- [`NoSuchElementException`](./Exception/NoSuchElementException.md)



***

### removeLast

Retrieves and removes the tail of this queue.

```php
public removeLast(): \Ramsey\Collection\T
```

This method differs from `pollLast()` only in that it throws an exception
if this queue is empty.







**Return Value:**

the last element in this queue.



**Throws:**
<p>if this queue is empty.</p>

- [`NoSuchElementException`](./Exception/NoSuchElementException.md)



***

### pollFirst

Retrieves and removes the head of this queue, or returns `null` if this
queue is empty.

```php
public pollFirst(): \Ramsey\Collection\T|null
```









**Return Value:**

the head of this queue, or `null` if this queue is empty.




***

### pollLast

Retrieves and removes the tail of this queue, or returns `null` if this
queue is empty.

```php
public pollLast(): \Ramsey\Collection\T|null
```









**Return Value:**

the tail of this queue, or `null` if this queue is empty.




***

### firstElement

Retrieves, but does not remove, the head of this queue.

```php
public firstElement(): \Ramsey\Collection\T
```

This method differs from `peekFirst()` only in that it throws an
exception if this queue is empty.







**Return Value:**

the head of this queue.



**Throws:**
<p>if this queue is empty.</p>

- [`NoSuchElementException`](./Exception/NoSuchElementException.md)



***

### lastElement

Retrieves, but does not remove, the tail of this queue.

```php
public lastElement(): \Ramsey\Collection\T
```

This method differs from `peekLast()` only in that it throws an exception
if this queue is empty.







**Return Value:**

the tail of this queue.



**Throws:**
<p>if this queue is empty.</p>

- [`NoSuchElementException`](./Exception/NoSuchElementException.md)



***

### peekFirst

Retrieves, but does not remove, the head of this queue, or returns `null`
if this queue is empty.

```php
public peekFirst(): \Ramsey\Collection\T|null
```









**Return Value:**

the head of this queue, or `null` if this queue is empty.




***

### peekLast

Retrieves, but does not remove, the tail of this queue, or returns `null`
if this queue is empty.

```php
public peekLast(): \Ramsey\Collection\T|null
```









**Return Value:**

the tail of this queue, or `null` if this queue is empty.




***


## Inherited methods


### clear

Removes all items from this array.

```php
public clear(): void
```












***

### toArray

Returns a native PHP array representation of this array object.

```php
public toArray(): array&lt;array-key,\Ramsey\Collection\T&gt;
```












***

### isEmpty

Returns `true` if this array is empty.

```php
public isEmpty(): bool
```












***

### add

Ensures that this queue contains the specified element (optional
operation).

```php
public add(\Ramsey\Collection\T $element): bool
```

Returns `true` if this queue changed as a result of the call. (Returns
`false` if this queue does not permit duplicates and already contains the
specified element.)

Queues that support this operation may place limitations on what elements
may be added to this queue. In particular, some queues will refuse to add
`null` elements, and others will impose restrictions on the type of
elements that may be added. Queue classes should clearly specify in their
documentation any restrictions on what elements may be added.

If a queue refuses to add a particular element for any reason other than
that it already contains the element, it must throw an exception (rather
than returning `false`). This preserves the invariant that a queue always
contains the specified element after this call returns.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\Ramsey\Collection\T** | The element to add to this queue. |


**Return Value:**

`true` if this queue changed as a result of the call.



**Throws:**
<p>if a queue refuses to add a particular element
for any reason other than that it already contains the element.
Implementations should use a more-specific exception that extends
<code class="prettyprint">\RuntimeException</code>.</p>

- [`RuntimeException`](../../RuntimeException.md)



**See Also:**

* \Ramsey\Collection\self::offer() - 

***

### element

Retrieves, but does not remove, the head of this queue.

```php
public element(): \Ramsey\Collection\T
```

This method differs from `peek()` only in that it throws an exception if
this queue is empty.







**Return Value:**

the head of this queue.



**Throws:**
<p>if this queue is empty.</p>

- [`NoSuchElementException`](./Exception/NoSuchElementException.md)



**See Also:**

* \Ramsey\Collection\self::peek() - 

***

### offer

Inserts the specified element into this queue if it is possible to do so
immediately without violating capacity restrictions.

```php
public offer(\Ramsey\Collection\T $element): bool
```

When using a capacity-restricted queue, this method is generally
preferable to `add()`, which can fail to insert an element only by
throwing an exception.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\Ramsey\Collection\T** | The element to add to this queue. |


**Return Value:**

`true` if the element was added to this queue, else `false`.




**See Also:**

* \Ramsey\Collection\self::add() - 

***

### peek

Retrieves, but does not remove, the head of this queue, or returns `null`
if this queue is empty.

```php
public peek(): \Ramsey\Collection\T|null
```









**Return Value:**

the head of this queue, or `null` if this queue is empty.




**See Also:**

* \Ramsey\Collection\self::element() - 

***

### poll

Retrieves and removes the head of this queue, or returns `null`
if this queue is empty.

```php
public poll(): \Ramsey\Collection\T|null
```









**Return Value:**

the head of this queue, or `null` if this queue is empty.




**See Also:**

* \Ramsey\Collection\self::remove() - 

***

### remove

Retrieves and removes the head of this queue.

```php
public remove(): \Ramsey\Collection\T
```

This method differs from `poll()` only in that it throws an exception if
this queue is empty.







**Return Value:**

the head of this queue.



**Throws:**
<p>if this queue is empty.</p>

- [`NoSuchElementException`](./Exception/NoSuchElementException.md)



**See Also:**

* \Ramsey\Collection\self::poll() - 

***

### getType

Returns the type associated with this queue.

```php
public getType(): string
```












***


***
> Automatically generated on 2025-03-18
