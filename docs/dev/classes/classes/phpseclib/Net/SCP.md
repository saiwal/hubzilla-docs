
# SCP

Pure-PHP implementations of SCP.



* Full name: `\phpseclib\Net\SCP`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`SOURCE_LOCAL_FILE`|public| |1|
|`SOURCE_STRING`|public| |2|
|`MODE_SSH1`|public| |1|
|`MODE_SSH2`|public| |2|

## Properties


### ssh

SSH Object

```php
public object $ssh
```






***

### packet_size

Packet Size

```php
public int $packet_size
```






***

### mode

Mode

```php
public int $mode
```






***

## Methods


### __construct

Default Constructor.

```php
public __construct(\phpseclib\Net\SSH1|\phpseclib\Net\SSH2 $ssh): \phpseclib\Net\SCP
```

Connects to an SSH server






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ssh` | **\phpseclib\Net\SSH1&#124;\phpseclib\Net\SSH2** |  |





***

### put

Uploads a file to the SCP server.

```php
public put(string $remote_file, string $data, int $mode = self::SOURCE_STRING, callable $callback = null): bool
```

By default, \phpseclib\Net\SCP::put() does not read from the local filesystem.  $data is dumped directly into $remote_file.
So, for example, if you set $data to 'filename.ext' and then do \phpseclib\Net\SCP::get(), you will get a file, twelve bytes
long, containing 'filename.ext' as its contents.

Setting $mode to self::SOURCE_LOCAL_FILE will change the above behavior.  With self::SOURCE_LOCAL_FILE, $remote_file will
contain as many bytes as filename.ext does on your local filesystem.  If your filename.ext is 1MB then that is how
large $remote_file will be, as well.

Currently, only binary mode is supported.  As such, if the line endings need to be adjusted, you will need to take
care of that, yourself.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$remote_file` | **string** |  |
| `$data` | **string** |  |
| `$mode` | **int** |  |
| `$callback` | **callable** |  |





***

### get

Downloads a file from the SCP server.

```php
public get(string $remote_file, string $local_file = false): mixed
```

Returns a string containing the contents of $remote_file if $local_file is left undefined or a boolean false if
the operation was unsuccessful.  If $local_file is defined, returns true or false depending on the success of the
operation






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$remote_file` | **string** |  |
| `$local_file` | **string** |  |





***

### _send

Sends a packet to an SSH server

```php
public _send(string $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





***

### _receive

Receives a packet from an SSH server

```php
public _receive(): string
```












***

### _close

Closes the connection to an SSH server

```php
public _close(): mixed
```












***


***
> Automatically generated on 2025-03-15
