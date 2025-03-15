***

# WildcardEmitter

This class is an EventEmitter with support for wildcard event handlers.

What this means is that you can emit events like this:

  emit('change:firstName')

and listen to this event like this:

  on('change:*')

A few notes:

- Wildcards only work at the end of an event name.
- Currently you can only use 1 wildcard.
- Using ":" as a separator is optional, but it's highly recommended to use
  some kind of separator.

The WildcardEmitter is a bit slower than the regular Emitter. If your code
must be very high performance, it might be better to try to use the other
emitter. For most usage the difference is negligible though.

* Full name: `\Sabre\Event\WildcardEmitter`
* This class implements:
[`\Sabre\Event\EmitterInterface`](./EmitterInterface.md)






## Inherited methods


### on

Subscribe to an event.

```php
public on(string $eventName, callable $callBack, int $priority = 100): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$eventName` | **string** |  |
| `$callBack` | **callable** |  |
| `$priority` | **int** |  |





***

### once

Subscribe to an event exactly once.

```php
public once(string $eventName, callable $callBack, int $priority = 100): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$eventName` | **string** |  |
| `$callBack` | **callable** |  |
| `$priority` | **int** |  |





***

### emit

Emits an event.

```php
public emit(string $eventName, array $arguments = [], callable $continueCallBack = null): bool
```

This method will return true if 0 or more listeners were successfully
handled. false is returned if one of the events broke the event chain.

If the continueCallBack is specified, this callback will be called every
time before the next event handler is called.

If the continueCallback returns false, event propagation stops. This
allows you to use the eventEmitter as a means for listeners to implement
functionality in your application, and break the event loop as soon as
some condition is fulfilled.

Note that returning false from an event subscriber breaks propagation
and returns false, but if the continue-callback stops propagation, this
is still considered a 'successful' operation and returns true.

Lastly, if there are 5 event handlers for an event. The continueCallback
will be called at most 4 times.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$eventName` | **string** |  |
| `$arguments` | **array** |  |
| `$continueCallBack` | **callable** |  |





***

### listeners

Returns the list of listeners for an event.

```php
public listeners(string $eventName): callable[]
```

The list is returned as an array, and the list of events are sorted by
their priority.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$eventName` | **string** |  |





***

### removeListener

Removes a specific listener from an event.

```php
public removeListener(string $eventName, callable $listener): bool
```

If the listener could not be found, this method will return false. If it
was removed it will return true.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$eventName` | **string** |  |
| `$listener` | **callable** |  |





***

### removeAllListeners

Removes all listeners.

```php
public removeAllListeners(string $eventName = null): mixed
```

If the eventName argument is specified, all listeners for that event are
removed. If it is not specified, every listener for every event is
removed.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$eventName` | **string** |  |





***


***
> Automatically generated on 2025-03-15
