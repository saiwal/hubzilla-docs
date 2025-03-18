
# Stream

SFTP Stream Wrapper



* Full name: `\phpseclib\Net\SFTP\Stream`



## Properties


### instances

SFTP instances

```php
public static array $instances
```

Rather than re-create the connection we re-use instances if possible

* This property is **static**.


***

### sftp

SFTP instance

```php
public object $sftp
```






***

### path

Path

```php
public string $path
```






***

### mode

Mode

```php
public string $mode
```






***

### pos

Position

```php
public int $pos
```






***

### size

Size

```php
public int $size
```






***

### entries

Directory entries

```php
public array $entries
```






***

### eof

EOF flag

```php
public bool $eof
```






***

### context

Context resource

```php
public resource $context
```

Technically this needs to be publically accessible so PHP can set it directly




***

### notification

Notification callback function

```php
public callable $notification
```






***

## Methods


### register

Registers this class as a URL wrapper.

```php
public static register(string $protocol = &#039;sftp&#039;): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$protocol` | **string** | The wrapper name to be registered. |


**Return Value:**

True on success, false otherwise.




***

### __construct

The Constructor

```php
public __construct(): mixed
```












***

### _parse_path

Path Parser

```php
public _parse_path(string $path): string
```

Extract a path from a URI and actually connect to an SSH server if appropriate

If "notification" is set as a context parameter the message code for successful login is
NET_SSH2_MSG_USERAUTH_SUCCESS. For a failed login it's NET_SSH2_MSG_USERAUTH_FAILURE.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### _stream_open

Opens file or URL

```php
public _stream_open(string $path, string $mode, int $options, string& $opened_path): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$mode` | **string** |  |
| `$options` | **int** |  |
| `$opened_path` | **string** |  |





***

### _stream_read

Read from stream

```php
public _stream_read(int $count): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$count` | **int** |  |





***

### _stream_write

Write to stream

```php
public _stream_write(string $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





***

### _stream_tell

Retrieve the current position of a stream

```php
public _stream_tell(): int
```












***

### _stream_eof

Tests for end-of-file on a file pointer

```php
public _stream_eof(): bool
```

In my testing there are four classes functions that normally effect the pointer:
fseek, fputs  / fwrite, fgets / fread and ftruncate.

Only fgets / fread, however, results in feof() returning true. do fputs($fp, 'aaa') on a blank file and feof()
will return false. do fread($fp, 1) and feof() will then return true. do fseek($fp, 10) on ablank file and feof()
will return false. do fread($fp, 1) and feof() will then return true.










***

### _stream_seek

Seeks to specific location in a stream

```php
public _stream_seek(int $offset, int $whence): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset` | **int** |  |
| `$whence` | **int** |  |





***

### _stream_metadata

Change stream options

```php
public _stream_metadata(string $path, int $option, mixed $var): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$option` | **int** |  |
| `$var` | **mixed** |  |





***

### _stream_cast

Retrieve the underlaying resource

```php
public _stream_cast(int $cast_as): resource
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cast_as` | **int** |  |





***

### _stream_lock

Advisory file locking

```php
public _stream_lock(int $operation): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$operation` | **int** |  |





***

### _rename

Renames a file or directory

```php
public _rename(string $path_from, string $path_to): bool
```

Attempts to rename oldname to newname, moving it between directories if necessary.
If newname exists, it will be overwritten.  This is a departure from what \phpseclib\Net\SFTP
does.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path_from` | **string** |  |
| `$path_to` | **string** |  |





***

### _dir_opendir

Open directory handle

```php
public _dir_opendir(string $path, int $options): bool
```

The only $options is "whether or not to enforce safe_mode (0x04)". Since safe mode was deprecated in 5.3 and
removed in 5.4 I'm just going to ignore it.

Also, nlist() is the best that this function is realistically going to be able to do. When an SFTP client
sends a SSH_FXP_READDIR packet you don't generally get info on just one file but on multiple files. Quoting
the SFTP specs:

   The SSH_FXP_NAME response has the following format:

       uint32     id
       uint32     count
       repeats count times:
               string     filename
               string     longname
               ATTRS      attrs






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$options` | **int** |  |





***

### _dir_readdir

Read entry from directory handle

```php
public _dir_readdir(): mixed
```












***

### _dir_rewinddir

Rewind directory handle

```php
public _dir_rewinddir(): bool
```












***

### _dir_closedir

Close directory handle

```php
public _dir_closedir(): bool
```












***

### _mkdir

Create a directory

```php
public _mkdir(string $path, int $mode, int $options): bool
```

Only valid $options is STREAM_MKDIR_RECURSIVE






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$mode` | **int** |  |
| `$options` | **int** |  |





***

### _rmdir

Removes a directory

```php
public _rmdir(string $path, int $options): bool
```

Only valid $options is STREAM_MKDIR_RECURSIVE per <http://php.net/streamwrapper.rmdir>, however,
<http://php.net/rmdir>  does not have a $recursive parameter as mkdir() does so I don't know how
STREAM_MKDIR_RECURSIVE is supposed to be set. Also, when I try it out with rmdir() I get 8 as
$options. What does 8 correspond to?






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$options` | **int** |  |





***

### _stream_flush

Flushes the output

```php
public _stream_flush(): bool
```

See <http://php.net/fflush>. Always returns true because \phpseclib\Net\SFTP doesn't cache stuff before writing










***

### _stream_stat

Retrieve information about a file resource

```php
public _stream_stat(): mixed
```












***

### _unlink

Delete a file

```php
public _unlink(string $path): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### _url_stat

Retrieve information about a file

```php
public _url_stat(string $path, int $flags): mixed
```

Ignores the STREAM_URL_STAT_QUIET flag because the entirety of \phpseclib\Net\SFTP\Stream is quiet by default
might be worthwhile to reconstruct bits 12-16 (ie. the file type) if mode doesn't have them but we'll
cross that bridge when and if it's reached






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$flags` | **int** |  |





***

### _stream_truncate

Truncate stream

```php
public _stream_truncate(int $new_size): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$new_size` | **int** |  |





***

### _stream_set_option

Change stream options

```php
public _stream_set_option(int $option, int $arg1, int $arg2): bool
```

STREAM_OPTION_WRITE_BUFFER isn't supported for the same reason stream_flush isn't.
The other two aren't supported because of limitations in \phpseclib\Net\SFTP.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$option` | **int** |  |
| `$arg1` | **int** |  |
| `$arg2` | **int** |  |





***

### _stream_close

Close an resource

```php
public _stream_close(): mixed
```












***

### __call

__call Magic Method

```php
public __call(string $name, array $arguments): mixed
```

When you're utilizing an SFTP stream you're not calling the methods in this class directly - PHP is calling them for you.
Which kinda begs the question... what methods is PHP calling and what parameters is it passing to them? This function
lets you figure that out.

If NET_SFTP_STREAM_LOGGING is defined all calls will be output on the screen and then (regardless of whether or not
NET_SFTP_STREAM_LOGGING is enabled) the parameters will be passed through to the appropriate method.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$arguments` | **array** |  |





***


***
> Automatically generated on 2025-03-18
