***

# SFTP

Pure-PHP implementations of SFTP.



* Full name: `\phpseclib\Net\SFTP`
* Parent class: [`\phpseclib\Net\SSH2`](./SSH2.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`CHANNEL`|public| |0x100|
|`SOURCE_LOCAL_FILE`|public| |1|
|`SOURCE_STRING`|public| |2|
|`SOURCE_CALLBACK`|public| |16|
|`RESUME`|public| |4|
|`RESUME_START`|public| |8|

## Properties


### packet_types

Packet Types

```php
public array $packet_types
```





**See Also:**

* \phpseclib\Net\self::__construct() - 

***

### status_codes

Status Codes

```php
public array $status_codes
```





**See Also:**

* \phpseclib\Net\self::__construct() - 

***

### use_request_id

The Request ID

```php
public bool $use_request_id
```

The request ID exists in the off chance that a packet is sent out-of-order.  Of course, this library doesn't support
concurrent actions, so it's somewhat academic, here.



**See Also:**

* \phpseclib\Net\self::_send_sftp_packet() - 

***

### packet_type

The Packet Type

```php
public int $packet_type
```

The request ID exists in the off chance that a packet is sent out-of-order.  Of course, this library doesn't support
concurrent actions, so it's somewhat academic, here.



**See Also:**

* \phpseclib\Net\self::_get_sftp_packet() - 

***

### packet_buffer

Packet Buffer

```php
public string $packet_buffer
```





**See Also:**

* \phpseclib\Net\self::_get_sftp_packet() - 

***

### extensions

Extensions supported by the server

```php
public array $extensions
```





**See Also:**

* \phpseclib\Net\self::_initChannel() - 

***

### version

Server SFTP version

```php
public int $version
```





**See Also:**

* \phpseclib\Net\self::_initChannel() - 

***

### defaultVersion

Default Server SFTP version

```php
public int $defaultVersion
```





**See Also:**

* \phpseclib\Net\self::_initChannel() - 

***

### preferredVersion

Preferred SFTP version

```php
public int $preferredVersion
```





**See Also:**

* \phpseclib\Net\self::_initChannel() - 

***

### pwd

Current working directory

```php
public string $pwd
```





**See Also:**

* \phpseclib\Net\self::realpath() - * \phpseclib\Net\self::chdir() - 

***

### packet_type_log

Packet Type Log

```php
public array $packet_type_log
```





**See Also:**

* \phpseclib\Net\self::getLog() - 

***

### packet_log

Packet Log

```php
public array $packet_log
```





**See Also:**

* \phpseclib\Net\self::getLog() - 

***

### sftp_errors

Error information

```php
public array $sftp_errors
```





**See Also:**

* \phpseclib\Net\self::getSFTPErrors() - * \phpseclib\Net\self::getLastSFTPError() - 

***

### stat_cache

Stat Cache

```php
public array $stat_cache
```

Rather than always having to open a directory and close it immediately there after to see if a file is a directory
we'll cache the results.



**See Also:**

* \phpseclib\Net\self::_update_stat_cache() - * \phpseclib\Net\self::_remove_from_stat_cache() - * \phpseclib\Net\self::_query_stat_cache() - 

***

### max_sftp_packet

Max SFTP Packet Size

```php
public array $max_sftp_packet
```





**See Also:**

* \phpseclib\Net\self::__construct() - * \phpseclib\Net\self::get() - 

***

### use_stat_cache

Stat Cache Flag

```php
public bool $use_stat_cache
```





**See Also:**

* \phpseclib\Net\self::disableStatCache() - * \phpseclib\Net\self::enableStatCache() - 

***

### sortOptions

Sort Options

```php
public array $sortOptions
```





**See Also:**

* \phpseclib\Net\self::_comparator() - * \phpseclib\Net\self::setListOrder() - 

***

### canonicalize_paths

Canonicalization Flag

```php
public bool $canonicalize_paths
```

Determines whether or not paths should be canonicalized before being
passed on to the remote server.



**See Also:**

* \phpseclib\Net\self::enablePathCanonicalization() - * \phpseclib\Net\self::disablePathCanonicalization() - * \phpseclib\Net\self::realpath() - 

***

### requestBuffer

Request Buffers

```php
public array $requestBuffer
```





**See Also:**

* \phpseclib\Net\self::_get_sftp_packet() - 

***

### preserveTime

Preserve timestamps on file downloads / uploads

```php
public bool $preserveTime
```





**See Also:**

* \phpseclib\Net\self::get() - * \phpseclib\Net\self::put() - 

***

### allow_arbitrary_length_packets

Arbitrary Length Packets Flag

```php
public bool $allow_arbitrary_length_packets
```

Determines whether or not packets of any length should be allowed,
in cases where the server chooses the packet length (such as
directory listings). By default, packets are only allowed to be
256 * 1024 bytes (SFTP_MAX_MSG_LENGTH from OpenSSH's sftp-common.h)



**See Also:**

* \phpseclib\Net\self::enableArbitraryLengthPackets() - * \phpseclib\Net\self::_get_sftp_packet() - 

***

### channel_close

Was the last packet due to the channels being closed or not?

```php
public bool $channel_close
```





**See Also:**

* \phpseclib\Net\self::get() - * \phpseclib\Net\self::get_sftp_packet() - 

***

### partial_init

Has the SFTP channel been partially negotiated?

```php
public bool $partial_init
```






***

### attributes

http://tools.ietf.org/html/draft-ietf-secsh-filexfer-13#section-7.1
the order, in this case, matters quite a lot - see \phpseclib3\Net\SFTP::_parseAttributes() to understand why

```php
public array $attributes
```






***

### open_flags



```php
public array $open_flags
```






***

### open_flags5

SFTPv5+ changed the flags up:
https://datatracker.ietf.org/doc/html/draft-ietf-secsh-filexfer-13#section-8.1.1.3

```php
public array $open_flags5
```






***

### file_types

http://tools.ietf.org/html/draft-ietf-secsh-filexfer-04#section-5.2
see \phpseclib\Net\SFTP::_parseLongname() for an explanation

```php
public array $file_types
```






***

## Methods


### __construct

Default Constructor.

```php
public __construct(string $host, int $port = 22, int $timeout = 10): \phpseclib\Net\SFTP
```

Connects to an SFTP server






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$host` | **string** |  |
| `$port` | **int** |  |
| `$timeout` | **int** |  |





***

### _precheck

Check a few things before SFTP functions are called

```php
public _precheck(): bool
```












***

### _partial_init_sftp_connection

Partially initialize an SFTP connection

```php
public _partial_init_sftp_connection(): bool
```












***

### _init_sftp_connection

(Re)initializes the SFTP channel

```php
public _init_sftp_connection(): bool
```












***

### disableStatCache

Disable the stat cache

```php
public disableStatCache(): mixed
```












***

### enableStatCache

Enable the stat cache

```php
public enableStatCache(): mixed
```












***

### clearStatCache

Clear the stat cache

```php
public clearStatCache(): mixed
```












***

### enablePathCanonicalization

Enable path canonicalization

```php
public enablePathCanonicalization(): mixed
```












***

### disablePathCanonicalization

Disable path canonicalization

```php
public disablePathCanonicalization(): mixed
```

If this is enabled then $sftp->pwd() will not return the canonicalized absolute path










***

### enableArbitraryLengthPackets

Enable arbitrary length packets

```php
public enableArbitraryLengthPackets(): mixed
```












***

### disableArbitraryLengthPackets

Disable arbitrary length packets

```php
public disableArbitraryLengthPackets(): mixed
```












***

### pwd

Returns the current directory name

```php
public pwd(): mixed
```












***

### _logError

Logs errors

```php
public _logError(string $response, int $status = -1): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$response` | **string** |  |
| `$status` | **int** |  |





***

### realpath

Returns canonicalized absolute pathname

```php
public realpath(string $path): mixed
```

realpath() expands all symbolic links and resolves references to '/./', '/../' and extra '/' characters in the input
path and returns the canonicalized absolute pathname.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### _realpath

Canonicalize the Server-Side Path Name

```php
public _realpath(string $path): mixed
```

SFTP doesn't provide a mechanism by which the current working directory can be changed, so we'll emulate it.  Returns
the absolute (canonicalized) path.

If canonicalize_paths has been disabled using disablePathCanonicalization(), $path is returned as-is.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





**See Also:**

* \phpseclib\Net\self::chdir() - * \phpseclib\Net\self::disablePathCanonicalization() - 

***

### chdir

Changes the current directory

```php
public chdir(string $dir): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dir` | **string** |  |





***

### nlist

Returns a list of files in the given directory

```php
public nlist(string $dir = &#039;.&#039;, bool $recursive = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dir` | **string** |  |
| `$recursive` | **bool** |  |





***

### _nlist_helper

Helper method for nlist

```php
public _nlist_helper(string $dir, bool $recursive, string $relativeDir): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dir` | **string** |  |
| `$recursive` | **bool** |  |
| `$relativeDir` | **string** |  |





***

### rawlist

Returns a detailed list of files in the given directory

```php
public rawlist(string $dir = &#039;.&#039;, bool $recursive = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dir` | **string** |  |
| `$recursive` | **bool** |  |





***

### _list

Reads a list, be it detailed or not, of files in the given directory

```php
public _list(string $dir, bool $raw = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dir` | **string** |  |
| `$raw` | **bool** |  |





***

### _comparator

Compares two rawlist entries using parameters set by setListOrder()

```php
public _comparator(array $a, array $b): int
```

Intended for use with uasort()






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$a` | **array** |  |
| `$b` | **array** |  |





***

### setListOrder

Defines how nlist() and rawlist() will be sorted - if at all.

```php
public setListOrder(): mixed
```

If sorting is enabled directories and files will be sorted independently with
directories appearing before files in the resultant array that is returned.

Any parameter returned by stat is a valid sort parameter for this function.
Filename comparisons are case insensitive.

Examples:

$sftp->setListOrder('filename', SORT_ASC);
$sftp->setListOrder('size', SORT_DESC, 'filename', SORT_ASC);
$sftp->setListOrder(true);
   Separates directories from files but doesn't do any sorting beyond that
$sftp->setListOrder();
   Don't do any sort of sorting










***

### size

Returns the file size, in bytes, or false, on failure

```php
public size(string $filename): mixed
```

Files larger than 4GB will show up as being exactly 4GB.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |





***

### _update_stat_cache

Save files / directories to cache

```php
public _update_stat_cache(string $path, mixed $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$value` | **mixed** |  |





***

### _remove_from_stat_cache

Remove files / directories from cache

```php
public _remove_from_stat_cache(string $path): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### _query_stat_cache

Checks cache for path

```php
public _query_stat_cache(string $path): mixed
```

Mainly used by file_exists






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### stat

Returns general information about a file.

```php
public stat(string $filename): mixed
```

Returns an array on success and false otherwise.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |





***

### lstat

Returns general information about a file or symbolic link.

```php
public lstat(string $filename): mixed
```

Returns an array on success and false otherwise.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |





***

### _stat

Returns general information about a file or symbolic link

```php
public _stat(string $filename, int $type): mixed
```

Determines information without calling \phpseclib\Net\SFTP::realpath().
The second parameter can be either NET_SFTP_STAT or NET_SFTP_LSTAT.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |
| `$type` | **int** |  |





***

### truncate

Truncates a file to a given length

```php
public truncate(string $filename, int $new_size): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |
| `$new_size` | **int** |  |





***

### touch

Sets access and modification time of file.

```php
public touch(string $filename, int $time = null, int $atime = null): bool
```

If the file does not exist, it will be created.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |
| `$time` | **int** |  |
| `$atime` | **int** |  |





***

### chown

Changes file or directory owner

```php
public chown(string $filename, int|string $uid, bool $recursive = false): bool
```

$uid should be an int for SFTPv3 and a string for SFTPv4+. Ideally the string
would be of the form "user@dns_domain" but it does not need to be.
`$sftp->getSupportedVersions()['version']` will return the specific version
that's being used.

Returns true on success or false on error.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |
| `$uid` | **int&#124;string** |  |
| `$recursive` | **bool** |  |





***

### chgrp

Changes file or directory group

```php
public chgrp(string $filename, int|string $gid, bool $recursive = false): bool
```

$gid should be an int for SFTPv3 and a string for SFTPv4+. Ideally the string
would be of the form "user@dns_domain" but it does not need to be.
`$sftp->getSupportedVersions()['version']` will return the specific version
that's being used.

Returns true on success or false on error.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |
| `$gid` | **int&#124;string** |  |
| `$recursive` | **bool** |  |





***

### chmod

Set permissions on a file.

```php
public chmod(int $mode, string $filename, bool $recursive = false): mixed
```

Returns the new file permissions on success or false on error.
If $recursive is true than this just returns true or false.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mode` | **int** |  |
| `$filename` | **string** |  |
| `$recursive` | **bool** |  |





***

### _setstat

Sets information about a file

```php
public _setstat(string $filename, string $attr, bool $recursive): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |
| `$attr` | **string** |  |
| `$recursive` | **bool** |  |





***

### _setstat_recursive

Recursively sets information on directories on the SFTP server

```php
public _setstat_recursive(string $path, string $attr, int& $i): bool
```

Minimizes directory lookups and SSH_FXP_STATUS requests for speed.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$attr` | **string** |  |
| `$i` | **int** |  |





***

### readlink

Return the target of a symbolic link

```php
public readlink(string $link): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$link` | **string** |  |





***

### symlink

Create a symlink

```php
public symlink(string $target, string $link): bool
```

symlink() creates a symbolic link to the existing target with the specified name link.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$target` | **string** |  |
| `$link` | **string** |  |





***

### mkdir

Creates a directory.

```php
public mkdir(string $dir, int $mode = -1, bool $recursive = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dir` | **string** |  |
| `$mode` | **int** |  |
| `$recursive` | **bool** |  |





***

### _mkdir_helper

Helper function for directory creation

```php
public _mkdir_helper(string $dir, int $mode): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dir` | **string** |  |
| `$mode` | **int** |  |





***

### rmdir

Removes a directory.

```php
public rmdir(string $dir): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dir` | **string** |  |





***

### _read_put_responses

Reads multiple successive SSH_FXP_WRITE responses

```php
public _read_put_responses(int $i): bool
```

Sending an SSH_FXP_WRITE packet and immediately reading its response isn't as efficient as blindly sending out $i
SSH_FXP_WRITEs, in succession, and then reading $i responses.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$i` | **int** |  |





***

### _close_handle

Close handle

```php
public _close_handle(string $handle): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$handle` | **string** |  |





***

### get

Downloads a file from the SFTP server.

```php
public get(string $remote_file, string $local_file = false, int $offset, int $length = -1, callable|null $progressCallback = null): mixed
```

Returns a string containing the contents of $remote_file if $local_file is left undefined or a boolean false if
the operation was unsuccessful.  If $local_file is defined, returns true or false depending on the success of the
operation.

$offset and $length can be used to download files in chunks.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$remote_file` | **string** |  |
| `$local_file` | **string** |  |
| `$offset` | **int** |  |
| `$length` | **int** |  |
| `$progressCallback` | **callable&#124;null** |  |





***

### delete

Deletes a file on the SFTP server.

```php
public delete(string $path, bool $recursive = true): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$recursive` | **bool** |  |





***

### _delete_recursive

Recursively deletes directories on the SFTP server

```php
public _delete_recursive(string $path, int& $i): bool
```

Minimizes directory lookups and SSH_FXP_STATUS requests for speed.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$i` | **int** |  |





***

### file_exists

Checks whether a file or directory exists

```php
public file_exists(string $path): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### is_dir

Tells whether the filename is a directory

```php
public is_dir(string $path): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### is_file

Tells whether the filename is a regular file

```php
public is_file(string $path): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### is_link

Tells whether the filename is a symbolic link

```php
public is_link(string $path): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### is_readable

Tells whether a file exists and is readable

```php
public is_readable(string $path): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### is_writable

Tells whether the filename is writable

```php
public is_writable(string $path): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### is_writeable

Tells whether the filename is writeable

```php
public is_writeable(string $path): bool
```

Alias of is_writable






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### fileatime

Gets last access time of file

```php
public fileatime(string $path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### filemtime

Gets file modification time

```php
public filemtime(string $path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### fileperms

Gets file permissions

```php
public fileperms(string $path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### fileowner

Gets file owner

```php
public fileowner(string $path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### filegroup

Gets file group

```php
public filegroup(string $path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### filesize

Gets file size

```php
public filesize(string $path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### filetype

Gets file type

```php
public filetype(string $path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### _get_stat_cache_prop

Return a stat properity

```php
public _get_stat_cache_prop(string $path, string $prop): mixed
```

Uses cache if appropriate.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$prop` | **string** |  |





***

### _get_lstat_cache_prop

Return an lstat properity

```php
public _get_lstat_cache_prop(string $path, string $prop): mixed
```

Uses cache if appropriate.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$prop` | **string** |  |





***

### _get_xstat_cache_prop

Return a stat or lstat properity

```php
public _get_xstat_cache_prop(string $path, string $prop, mixed $type): mixed
```

Uses cache if appropriate.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$prop` | **string** |  |
| `$type` | **mixed** |  |





***

### rename

Renames a file or a directory on the SFTP server.

```php
public rename(string $oldname, string $newname): bool
```

If the file already exists this will return false






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$oldname` | **string** |  |
| `$newname` | **string** |  |





***

### _parseTime

Parse Time

```php
public _parseTime(string $key, int $flags, string& $response): array
```

See '7.7.  Times' of draft-ietf-secsh-filexfer-13 for more info.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** |  |
| `$flags` | **int** |  |
| `$response` | **string** |  |





***

### _parseAttributes

Parse Attributes

```php
public _parseAttributes(string& $response): array
```

See '7.  File Attributes' of draft-ietf-secsh-filexfer-13 for more info.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$response` | **string** |  |





***

### _parseMode

Attempt to identify the file type

```php
public _parseMode(int $mode): int
```

Quoting the SFTP RFC, "Implementations MUST NOT send bits that are not defined" but they seem to anyway






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mode` | **int** |  |





***

### _parseLongname

Parse Longname

```php
public _parseLongname(string $longname): mixed
```

SFTPv3 doesn't provide any easy way of identifying a file type.  You could try to open
a file as a directory and see if an error is returned or you could try to parse the
SFTPv3-specific longname field of the SSH_FXP_NAME packet.  That's what this function does.
The result is returned using the
{@link http://tools.ietf.org/html/draft-ietf-secsh-filexfer-04#section-5.2}.

If the longname is in an unrecognized format bool(false) is returned.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$longname` | **string** |  |





***

### _send_sftp_packet

Sends SFTP Packets

```php
public _send_sftp_packet(int $type, string $data, int $request_id = 1): bool
```

See '6. General Packet Format' of draft-ietf-secsh-filexfer-13 for more info.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **int** |  |
| `$data` | **string** |  |
| `$request_id` | **int** |  |





**See Also:**

* \phpseclib\Net\self::_get_sftp_packet() - * \phpseclib\Net\self::_send_channel_packet() - 

***

### _reset_connection

Resets a connection for re-use

```php
public _reset_connection(int $reason): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reason` | **int** |  |





***

### _get_sftp_packet

Receives SFTP Packets

```php
public _get_sftp_packet(mixed $request_id = null): string
```

See '6. General Packet Format' of draft-ietf-secsh-filexfer-13 for more info.

Incidentally, the number of SSH_MSG_CHANNEL_DATA messages has no bearing on the number of SFTP packets present.
There can be one SSH_MSG_CHANNEL_DATA messages containing two SFTP packets or there can be two SSH_MSG_CHANNEL_DATA
messages containing one SFTP packet.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request_id` | **mixed** |  |





**See Also:**

* \phpseclib\Net\self::_send_sftp_packet() - 

***

### getSFTPLog

Returns a log of the packets that have been sent and received.

```php
public getSFTPLog(): string
```

Returns a string if NET_SFTP_LOGGING == NET_SFTP_LOG_COMPLEX, an array if NET_SFTP_LOGGING == NET_SFTP_LOG_SIMPLE and false if !defined('NET_SFTP_LOGGING')







**Return Value:**

or Array




***

### getSFTPErrors

Returns all errors on the SFTP layer

```php
public getSFTPErrors(): array
```












***

### getLastSFTPError

Returns the last error on the SFTP layer

```php
public getLastSFTPError(): string
```












***

### getSupportedVersions

Get supported SFTP versions

```php
public getSupportedVersions(): array
```












***

### getNegotiatedVersion

Get supported SFTP versions

```php
public getNegotiatedVersion(): array
```












***

### setPreferredVersion

Set preferred version

```php
public setPreferredVersion(int $version): mixed
```

If you're preferred version isn't supported then the highest supported
version of SFTP will be utilized. Set to null or false or int(0) to
unset the preferred version






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$version` | **int** |  |





***

### _disconnect

Disconnect

```php
public _disconnect(int $reason): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reason` | **int** |  |





***

### enableDatePreservation

Enable Date Preservation

```php
public enableDatePreservation(): mixed
```












***

### disableDatePreservation

Disable Date Preservation

```php
public disableDatePreservation(): mixed
```












***


## Inherited methods


### __construct

Default Constructor.

```php
public __construct(mixed $host, int $port = 22, int $timeout = 10): \phpseclib\Net\SSH2
```

$host can either be a string, representing the host, or a stream resource.
If $host is a stream resource then $port doesn't do anything, altho $timeout
still will be used






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$host` | **mixed** |  |
| `$port` | **int** |  |
| `$timeout` | **int** |  |





**See Also:**

* \phpseclib\Net\self::login() - 

***

### setCryptoEngine

Set Crypto Engine Mode

```php
public setCryptoEngine(int $engine): mixed
```

Possible $engine values:
CRYPT_MODE_INTERNAL, CRYPT_MODE_MCRYPT






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$engine` | **int** |  |





***

### sendIdentificationStringFirst

Send Identification String First

```php
public sendIdentificationStringFirst(): mixed
```

https://tools.ietf.org/html/rfc4253#section-4.2 says "when the connection has been established,
both sides MUST send an identification string". It does not say which side sends it first. In
theory it shouldn't matter but it is a fact of life that some SSH servers are simply buggy










***

### sendIdentificationStringLast

Send Identification String Last

```php
public sendIdentificationStringLast(): mixed
```

https://tools.ietf.org/html/rfc4253#section-4.2 says "when the connection has been established,
both sides MUST send an identification string". It does not say which side sends it first. In
theory it shouldn't matter but it is a fact of life that some SSH servers are simply buggy










***

### sendKEXINITFirst

Send SSH_MSG_KEXINIT First

```php
public sendKEXINITFirst(): mixed
```

https://tools.ietf.org/html/rfc4253#section-7.1 says "key exchange begins by each sending
sending the [SSH_MSG_KEXINIT] packet". It does not say which side sends it first. In theory
it shouldn't matter but it is a fact of life that some SSH servers are simply buggy










***

### sendKEXINITLast

Send SSH_MSG_KEXINIT Last

```php
public sendKEXINITLast(): mixed
```

https://tools.ietf.org/html/rfc4253#section-7.1 says "key exchange begins by each sending
sending the [SSH_MSG_KEXINIT] packet". It does not say which side sends it first. In theory
it shouldn't matter but it is a fact of life that some SSH servers are simply buggy










***

### _connect

Connect to an SSHv2 server

```php
public _connect(): bool
```












***

### _generate_identifier

Generates the SSH identifier

```php
public _generate_identifier(): string
```

You should overwrite this method in your own class if you want to use another identifier










***

### _key_exchange

Key Exchange

```php
public _key_exchange(string $kexinit_payload_server = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$kexinit_payload_server` | **string** | optional |





***

### _encryption_algorithm_to_key_size

Maps an encryption algorithm name to the number of key bytes.

```php
public _encryption_algorithm_to_key_size(string $algorithm): int|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$algorithm` | **string** | Name of the encryption algorithm |


**Return Value:**

Number of bytes as an integer or null for unknown




***

### _encryption_algorithm_to_crypt_instance

Maps an encryption algorithm name to an instance of a subclass of
\phpseclib\Crypt\Base.

```php
public _encryption_algorithm_to_crypt_instance(string $algorithm): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$algorithm` | **string** | Name of the encryption algorithm |


**Return Value:**

Instance of \phpseclib\Crypt\Base or null for unknown




***

### _bad_algorithm_candidate

Tests whether or not proposed algorithm has a potential for issues

```php
public _bad_algorithm_candidate(string $algorithm): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$algorithm` | **string** | Name of the encryption algorithm |





**See Also:**

* https://www.chiark.greenend.org.uk/~sgtatham/putty/wishlist/ssh2-aesctr-openssh.html - * https://bugzilla.mindrot.org/show_bug.cgi?id=1291 - 

***

### login

Login

```php
public login(string $username): bool
```

The $password parameter can be a plaintext password, a \phpseclib\Crypt\RSA object or an array






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |





**See Also:**

* \phpseclib\Net\self::_login() - 

***

### _login

Login Helper

```php
public _login(string $username): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |





**See Also:**

* \phpseclib\Net\self::_login_helper() - 

***

### _keyboard_interactive_login

Login via keyboard-interactive authentication

```php
public _keyboard_interactive_login(string $username, string $password): bool
```

See {@link http://tools.ietf.org/html/rfc4256} for details.  This is not a full-featured keyboard-interactive authenticator.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |
| `$password` | **string** |  |





***

### _keyboard_interactive_process

Handle the keyboard-interactive requests / responses.

```php
public _keyboard_interactive_process(): bool
```












***

### _ssh_agent_login

Login with an ssh-agent provided key

```php
public _ssh_agent_login(string $username, \phpseclib\System\SSH\Agent $agent): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |
| `$agent` | **\phpseclib\System\SSH\Agent** |  |





***

### getTimeout

Return the currently configured timeout

```php
public getTimeout(): int
```












***

### setTimeout

Set Timeout

```php
public setTimeout(mixed $timeout): mixed
```

$ssh->exec('ping 127.0.0.1'); on a Linux host will never return and will run indefinitely.  setTimeout() makes it so it'll timeout.
Setting $timeout to false or 0 will mean there is no timeout.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$timeout` | **mixed** |  |





***

### setKeepAlive

Set Keep Alive

```php
public setKeepAlive(int $interval): mixed
```

Sends an SSH2_MSG_IGNORE message every x seconds, if x is a positive non-zero number.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$interval` | **int** |  |





***

### getStdError

Get the output from stdError

```php
public getStdError(): mixed
```












***

### exec

Execute Command

```php
public exec(string $command, callable $callback = null): string
```

If $callback is set to false then \phpseclib\Net\SSH2::_get_channel_packet(self::CHANNEL_EXEC) will need to be called manually.
In all likelihood, this is not a feature you want to be taking advantage of.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$command` | **string** |  |
| `$callback` | **callable** |  |





***

### _initShell

Creates an interactive shell

```php
public _initShell(): bool
```












**See Also:**

* \phpseclib\Net\self::read() - * \phpseclib\Net\self::write() - 

***

### _get_interactive_channel

Return the channel to be used with read() / write()

```php
public _get_interactive_channel(): int
```












**See Also:**

* \phpseclib\Net\self::read() - * \phpseclib\Net\self::write() - 

***

### _get_open_channel

Return an available open channel

```php
public _get_open_channel(): int
```












***

### read

Returns the output of an interactive shell

```php
public read(string $expect = &#039;&#039;, int $mode = self::READ_SIMPLE): string|bool
```

Returns when there's a match for $expect, which can take the form of a string literal or,
if $mode == self::READ_REGEX, a regular expression.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$expect` | **string** |  |
| `$mode` | **int** |  |





**See Also:**

* \phpseclib\Net\self::write() - 

***

### write

Inputs a command into an interactive shell.

```php
public write(string $cmd): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cmd` | **string** |  |





**See Also:**

* \phpseclib\Net\self::read() - 

***

### startSubsystem

Start a subsystem.

```php
public startSubsystem(string $subsystem): bool
```

Right now only one subsystem at a time is supported. To support multiple subsystem's stopSubsystem() could accept
a string that contained the name of the subsystem, but at that point, only one subsystem of each type could be opened.
To support multiple subsystem's of the same name maybe it'd be best if startSubsystem() generated a new channel id and
returns that and then that that was passed into stopSubsystem() but that'll be saved for a future date and implemented
if there's sufficient demand for such a feature.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$subsystem` | **string** |  |





**See Also:**

* \phpseclib\Net\self::stopSubsystem() - 

***

### stopSubsystem

Stops a subsystem.

```php
public stopSubsystem(): bool
```












**See Also:**

* \phpseclib\Net\self::startSubsystem() - 

***

### reset

Closes a channel

```php
public reset(): mixed
```

If read() timed out you might want to just close the channel and have it auto-restart on the next read() call










***

### isTimeout

Is timeout?

```php
public isTimeout(): mixed
```

Did exec() or read() return because they timed out or because they encountered the end?










***

### disconnect

Disconnect

```php
public disconnect(): mixed
```












***

### __destruct

Destructor.

```php
public __destruct(): mixed
```

Will be called, automatically, if you're supporting just PHP5.  If you're supporting PHP4, you'll need to call
disconnect().










***

### isConnected

Is the connection still active?

```php
public isConnected(): bool
```












***

### isAuthenticated

Have you successfully been logged in?

```php
public isAuthenticated(): bool
```












***

### ping

Pings a server connection, or tries to reconnect if the connection has gone down

```php
public ping(): bool
```

Inspired by http://php.net/manual/en/mysqli.ping.php










***

### _reconnect

In situ reconnect method

```php
public _reconnect(): bool
```












***

### _reset_connection

Resets a connection for re-use

```php
public _reset_connection(int $reason): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reason` | **int** |  |





***

### _get_binary_packet

Gets Binary Packets

```php
public _get_binary_packet(mixed $skip_channel_filter = false): string
```

See '6. Binary Packet Protocol' of rfc4253 for more info.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$skip_channel_filter` | **mixed** |  |





**See Also:**

* \phpseclib\Net\self::_send_binary_packet() - 

***

### _filter

Filter Binary Packets

```php
public _filter(mixed $payload, mixed $skip_channel_filter): string
```

Because some binary packets need to be ignored...






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$payload` | **mixed** |  |
| `$skip_channel_filter` | **mixed** |  |





**See Also:**

* \phpseclib\Net\self::_get_binary_packet() - 

***

### enableQuietMode

Enable Quiet Mode

```php
public enableQuietMode(): mixed
```

Suppress stderr from output










***

### disableQuietMode

Disable Quiet Mode

```php
public disableQuietMode(): mixed
```

Show stderr in output










***

### isQuietModeEnabled

Returns whether Quiet Mode is enabled or not

```php
public isQuietModeEnabled(): bool
```












**See Also:**

* \phpseclib\Net\self::enableQuietMode() - * \phpseclib\Net\self::disableQuietMode() - 

***

### enablePTY

Enable request-pty when using exec()

```php
public enablePTY(): mixed
```












***

### disablePTY

Disable request-pty when using exec()

```php
public disablePTY(): mixed
```












***

### isPTYEnabled

Returns whether request-pty is enabled or not

```php
public isPTYEnabled(): bool
```












**See Also:**

* \phpseclib\Net\self::enablePTY() - * \phpseclib\Net\self::disablePTY() - 

***

### _get_channel_packet

Gets channel data

```php
public _get_channel_packet(int $client_channel, bool $skip_extended = false): mixed|bool
```

Returns the data as a string if it's available and false if not.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_channel` | **int** |  |
| `$skip_extended` | **bool** |  |





***

### _send_binary_packet

Sends Binary Packets

```php
public _send_binary_packet(string $data, string $logged = null): bool
```

See '6. Binary Packet Protocol' of rfc4253 for more info.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |
| `$logged` | **string** |  |





**See Also:**

* \phpseclib\Net\self::_get_binary_packet() - 

***

### _append_log

Logs data packets

```php
public _append_log(string $message_number, string $message): mixed
```

Makes sure that only the last 1MB worth of packets will be logged






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message_number` | **string** |  |
| `$message` | **string** |  |





***

### _send_channel_packet

Sends channel data

```php
public _send_channel_packet(int $client_channel, string $data): bool
```

Spans multiple SSH_MSG_CHANNEL_DATAs if appropriate






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_channel` | **int** |  |
| `$data` | **string** |  |





***

### _close_channel

Closes and flushes a channel

```php
public _close_channel(int $client_channel, bool $want_reply = false): bool
```

\phpseclib\Net\SSH2 doesn't properly close most channels.  For exec() channels are normally closed by the server
and for SFTP channels are presumably closed when the client disconnects.  This functions is intended
for SCP more than anything.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_channel` | **int** |  |
| `$want_reply` | **bool** |  |





***

### _disconnect

Disconnect

```php
public _disconnect(int $reason): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reason` | **int** |  |





***

### _string_shift

String Shift

```php
public _string_shift(string& $string, int $index = 1): string
```

Inspired by array_shift






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** |  |
| `$index` | **int** |  |





***

### _define_array

Define Array

```php
public _define_array(): mixed
```

Takes any number of arrays whose indices are integers and whose values are strings and defines a bunch of
named constants from it, using the value as the name of the constant and the index as the value of the constant.
If any of the constants that would be defined already exists, none of the constants will be defined.










***

### getLog

Returns a log of the packets that have been sent and received.

```php
public getLog(): array|false|string
```

Returns a string if NET_SSH2_LOGGING == self::LOG_COMPLEX, an array if NET_SSH2_LOGGING == self::LOG_SIMPLE and false if !defined('NET_SSH2_LOGGING')










***

### _format_log

Formats a log for printing

```php
public _format_log(array $message_log, array $message_number_log): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message_log` | **array** |  |
| `$message_number_log` | **array** |  |





***

### _format_log_helper

Helper function for _format_log

```php
public _format_log_helper(array $matches): string
```

For use with preg_replace_callback()






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### _on_channel_open

Helper function for agent->_on_channel_open()

```php
public _on_channel_open(): mixed
```

Used when channels are created to inform agent
of said channel opening. Must be called after
channel open confirmation received










***

### _array_intersect_first

Returns the first value of the intersection of two arrays or false if
the intersection is empty. The order is defined by the first parameter.

```php
public _array_intersect_first(array $array1, array $array2): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$array1` | **array** |  |
| `$array2` | **array** |  |


**Return Value:**

False if intersection is empty, else intersected value.




***

### getErrors

Returns all errors / debug messages on the SSH layer

```php
public getErrors(): string[]
```

If you are looking for messages from the SFTP layer, please see SFTP::getSFTPErrors()










***

### getLastError

Returns the last error received on the SSH layer

```php
public getLastError(): string
```

If you are looking for messages from the SFTP layer, please see SFTP::getLastSFTPError()










***

### getServerIdentification

Return the server identification.

```php
public getServerIdentification(): string
```












***

### getKexAlgorithms

Return a list of the key exchange algorithms the server supports.

```php
public getKexAlgorithms(): array
```












***

### getServerHostKeyAlgorithms

Return a list of the host key (public key) algorithms the server supports.

```php
public getServerHostKeyAlgorithms(): array
```












***

### getEncryptionAlgorithmsClient2Server

Return a list of the (symmetric key) encryption algorithms the server supports, when receiving stuff from the client.

```php
public getEncryptionAlgorithmsClient2Server(): array
```












***

### getEncryptionAlgorithmsServer2Client

Return a list of the (symmetric key) encryption algorithms the server supports, when sending stuff to the client.

```php
public getEncryptionAlgorithmsServer2Client(): array
```












***

### getMACAlgorithmsClient2Server

Return a list of the MAC algorithms the server supports, when receiving stuff from the client.

```php
public getMACAlgorithmsClient2Server(): array
```












***

### getMACAlgorithmsServer2Client

Return a list of the MAC algorithms the server supports, when sending stuff to the client.

```php
public getMACAlgorithmsServer2Client(): array
```












***

### getCompressionAlgorithmsClient2Server

Return a list of the compression algorithms the server supports, when receiving stuff from the client.

```php
public getCompressionAlgorithmsClient2Server(): array
```












***

### getCompressionAlgorithmsServer2Client

Return a list of the compression algorithms the server supports, when sending stuff to the client.

```php
public getCompressionAlgorithmsServer2Client(): array
```












***

### getLanguagesServer2Client

Return a list of the languages the server supports, when sending stuff to the client.

```php
public getLanguagesServer2Client(): array
```












***

### getLanguagesClient2Server

Return a list of the languages the server supports, when receiving stuff from the client.

```php
public getLanguagesClient2Server(): array
```












***

### getServerAlgorithms

Returns a list of algorithms the server supports

```php
public getServerAlgorithms(): array
```












***

### getSupportedKEXAlgorithms

Returns a list of KEX algorithms that phpseclib supports

```php
public getSupportedKEXAlgorithms(): array
```












***

### getSupportedHostKeyAlgorithms

Returns a list of host key algorithms that phpseclib supports

```php
public getSupportedHostKeyAlgorithms(): array
```












***

### getSupportedEncryptionAlgorithms

Returns a list of symmetric key algorithms that phpseclib supports

```php
public getSupportedEncryptionAlgorithms(): array
```












***

### getSupportedMACAlgorithms

Returns a list of MAC algorithms that phpseclib supports

```php
public getSupportedMACAlgorithms(): array
```












***

### getSupportedCompressionAlgorithms

Returns a list of compression algorithms that phpseclib supports

```php
public getSupportedCompressionAlgorithms(): array
```












***

### getAlgorithmsNegotiated

Return list of negotiated algorithms

```php
public getAlgorithmsNegotiated(): array
```

Uses the same format as https://www.php.net/ssh2-methods-negotiated










***

### setPreferredAlgorithms

Accepts an associative array with up to four parameters as described at
<https://www.php.net/manual/en/function.ssh2-connect.php>

```php
public setPreferredAlgorithms(array $methods): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$methods` | **array** |  |





***

### getBannerMessage

Returns the banner message.

```php
public getBannerMessage(): string
```

Quoting from the RFC, "in some jurisdictions, sending a warning message before
authentication may be relevant for getting legal protection."










***

### getServerPublicHostKey

Returns the server public host key.

```php
public getServerPublicHostKey(): mixed
```

Caching this the first time you connect to a server and checking the result on subsequent connections
is recommended.  Returns false if the server signature is not signed correctly with the public host key.










***

### getExitStatus

Returns the exit status of an SSH command or false.

```php
public getExitStatus(): false|int
```












***

### getWindowColumns

Returns the number of columns for the terminal window size.

```php
public getWindowColumns(): int
```












***

### getWindowRows

Returns the number of rows for the terminal window size.

```php
public getWindowRows(): int
```












***

### setWindowColumns

Sets the number of columns for the terminal window size.

```php
public setWindowColumns(int $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **int** |  |





***

### setWindowRows

Sets the number of rows for the terminal window size.

```php
public setWindowRows(int $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **int** |  |





***

### setWindowSize

Sets the number of columns and rows for the terminal window size.

```php
public setWindowSize(int $columns = 80, int $rows = 24): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$columns` | **int** |  |
| `$rows` | **int** |  |





***

### _updateLogHistory

Update packet types in log history

```php
public _updateLogHistory(string $old, string $new): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$old` | **string** |  |
| `$new` | **string** |  |





***

### getAuthMethodsToContinue

Return the list of authentication methods that may productively continue authentication.

```php
public getAuthMethodsToContinue(): array|null
```












**See Also:**

* https://tools.ietf.org/html/rfc4252#section-5.1 - 

***

### enableSmartMFA

Enables "smart" multi-factor authentication (MFA)

```php
public enableSmartMFA(): mixed
```












***

### disableSmartMFA

Disables "smart" multi-factor authentication (MFA)

```php
public disableSmartMFA(): mixed
```












***


***
> Automatically generated on 2025-03-15
