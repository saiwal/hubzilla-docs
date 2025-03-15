
# QueueInterface

A queue is a collection in which the entities in the collection are kept in
order.

The principal operations on the queue are the addition of entities to the end
(tail), also known as *enqueue*, and removal of entities from the front
(head), also known as *dequeue*. This makes the queue a first-in-first-out
(FIFO) data structure.

Besides basic array operations, queues provide additional insertion,
extraction, and inspection operations. Each of these methods exists in two
forms: one throws an exception if the operation fails, the other returns a
special value (either `null` or `false`, depending on the operation). The
latter form of the insert operation is designed specifically for use with
capacity-restricted `QueueInterface` implementations; in most
implementations, insert operations cannot fail.

<table>
<caption>Summary of QueueInterface methods</caption>
<thead>
<tr>
<td></td>
<td><em>Throws exception</em></td>
<td><em>Returns special value</em></td>
</tr>
</thead>
<tbody>
<tr>
<th>Insert</th>
<td><code>add()</code></td>
<td><code>offer()</code></td>
</tr>
<tr>
<th>Remove</th>
<td><code>remove()</code></td>
<td><code>poll()</code></td>
</tr>
<tr>
<th>Examine</th>
<td><code>element()</code></td>
<td><code>peek()</code></td>
</tr>
</tbody>
</table>

Queues typically, but do not necessarily, order elements in a FIFO
(first-in-first-out) manner. Among the exceptions are priority queues, which
order elements according to a supplied comparator, or the elements' natural
ordering, and LIFO queues (or stacks) which order the elements LIFO
(last-in-first-out). Whatever the ordering used, the head of the queue is
that element which would be removed by a call to remove() or poll(). In a
FIFO queue, all new elements are inserted at the tail of the queue. Other
kinds of queues may use different placement rules. Every `QueueInterface`
implementation must specify its ordering properties.

The `offer()` method inserts an element if possible, otherwise returning
`false`. This differs from the `add()` method, which can fail to add an
element only by throwing an unchecked exception. The `offer()` method is
designed for use when failure is a normal, rather than exceptional
occurrence, for example, in fixed-capacity (or "bounded") queues.

The `remove()` and `poll()` methods remove and return the head of the queue.
Exactly which element is removed from the queue is a function of the queue's
ordering policy, which differs from implementation to implementation. The
`remove()` and `poll()` methods differ only in their behavior when the queue
is empty: the `remove()` method throws an exception, while the `poll()`
method returns `null`.

The `element()` and `peek()` methods return, but do not remove, the head of
the queue.

`QueueInterface` implementations generally do not allow insertion of `null`
elements, although some implementations do not prohibit insertion of `null`.
Even in the implementations that permit it, `null` should not be inserted
into a queue, as `null` is also used as a special return value by the
`poll()` method to indicate that the queue contains no elements.

* Full name: `\Ramsey\Collection\QueueInterface`
* Parent interfaces: [`\Ramsey\Collection\ArrayInterface`](./ArrayInterface.md)


## Methods


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


***
> Automatically generated on 2025-03-15
