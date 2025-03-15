***

# Loop

A simple eventloop implementation.

This eventloop supports:
* nextTick
* setTimeout for delayed functions
* setInterval for repeating functions
* stream events using stream_select

* Full name: `\Sabre\Event\Loop\Loop`



## Properties


### running

Is the main loop active.

```php
protected bool $running
```






***

### timers

A list of timers, added by setTimeout.

```php
protected array $timers
```






***

### nextTick

A list of 'nextTick' callbacks.

```php
protected callable[] $nextTick
```






***

### readStreams

List of readable streams for stream_select, indexed by stream id.

```php
protected resource[] $readStreams
```






***

### writeStreams

List of writable streams for stream_select, indexed by stream id.

```php
protected resource[] $writeStreams
```






***

### readCallbacks

List of read callbacks, indexed by stream id.

```php
protected callable[] $readCallbacks
```






***

### writeCallbacks

List of write callbacks, indexed by stream id.

```php
protected callable[] $writeCallbacks
```






***

## Methods


### setTimeout

Executes a function after x seconds.

```php
public setTimeout(callable $cb, float $timeout): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cb` | **callable** |  |
| `$timeout` | **float** |  |





***

### setInterval

Executes a function every x seconds.

```php
public setInterval(callable $cb, float $timeout): array
```

The value this function returns can be used to stop the interval with
clearInterval.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cb` | **callable** |  |
| `$timeout` | **float** |  |





***

### clearInterval

Stops a running interval.

```php
public clearInterval(array $intervalId): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$intervalId` | **array** |  |





***

### nextTick

Runs a function immediately at the next iteration of the loop.

```php
public nextTick(callable $cb): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cb` | **callable** |  |





***

### addReadStream

Adds a read stream.

```php
public addReadStream(resource $stream, callable $cb): mixed
```

The callback will be called as soon as there is something to read from
the stream.

You MUST call removeReadStream after you are done with the stream, to
prevent the eventloop from never stopping.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stream` | **resource** |  |
| `$cb` | **callable** |  |





***

### addWriteStream

Adds a write stream.

```php
public addWriteStream(resource $stream, callable $cb): mixed
```

The callback will be called as soon as the system reports it's ready to
receive writes on the stream.

You MUST call removeWriteStream after you are done with the stream, to
prevent the eventloop from never stopping.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stream` | **resource** |  |
| `$cb` | **callable** |  |





***

### removeReadStream

Stop watching a stream for reads.

```php
public removeReadStream(resource $stream): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stream` | **resource** |  |





***

### removeWriteStream

Stop watching a stream for writes.

```php
public removeWriteStream(resource $stream): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stream` | **resource** |  |





***

### run

Runs the loop.

```php
public run(): mixed
```

This function will run continuously, until there's no more events to
handle.










***

### tick

Executes all pending events.

```php
public tick(bool $block = false): bool
```

If $block is turned true, this function will block until any event is
triggered.

If there are now timeouts, nextTick callbacks or events in the loop at
all, this function will exit immediately.

This function will return true if there are _any_ events left in the
loop after the tick.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$block` | **bool** |  |





***

### stop

Stops a running eventloop.

```php
public stop(): mixed
```












***

### runNextTicks

Executes all 'nextTick' callbacks.

```php
protected runNextTicks(): mixed
```

return void










***

### runTimers

Runs all pending timers.

```php
protected runTimers(): float|null
```

After running the timer callbacks, this function returns the number of
seconds until the next timer should be executed.

If there's no more pending timers, this function returns null.










***

### runStreams

Runs all pending stream events.

```php
protected runStreams(mixed $timeout): mixed
```

If $timeout is 0, it will return immediately. If $timeout is null, it
will wait indefinitely.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$timeout` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
