
# SSH1

Pure-PHP implementation of SSHv1.



* Full name: `\phpseclib\Net\SSH1`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`CIPHER_NONE`|public| |0|
|`CIPHER_IDEA`|public| |1|
|`CIPHER_DES`|public| |2|
|`CIPHER_3DES`|public| |3|
|`CIPHER_BROKEN_TSS`|public| |4|
|`CIPHER_BLOWFISH`|public| |6|
|`AUTH_RHOSTS`|public| |1|
|`AUTH_RSA`|public| |2|
|`AUTH_PASSWORD`|public| |3|
|`AUTH_RHOSTS_RSA`|public| |4|
|`TTY_OP_END`|public| |0|
|`RESPONSE_TYPE`|public| |1|
|`RESPONSE_DATA`|public| |2|
|`MASK_CONSTRUCTOR`|public| |0x1|
|`MASK_CONNECTED`|public| |0x2|
|`MASK_LOGIN`|public| |0x4|
|`MASK_SHELL`|public| |0x8|
|`LOG_SIMPLE`|public| |1|
|`LOG_COMPLEX`|public| |2|
|`LOG_REALTIME`|public| |3|
|`LOG_REALTIME_FILE`|public| |4|
|`LOG_MAX_SIZE`|public| |1048576|
|`READ_SIMPLE`|public| |1|
|`READ_REGEX`|public| |2|

## Properties


### identifier

The SSH identifier

```php
public string $identifier
```






***

### fsock

The Socket Object

```php
public object $fsock
```






***

### crypto

The cryptography object

```php
public object $crypto
```






***

### bitmap

Execution Bitmap

```php
public int $bitmap
```

The bits that are set represent functions that have been called already.  This is used to determine
if a requisite function has been successfully executed.  If not, an error should be thrown.




***

### server_key_public_exponent

The Server Key Public Exponent

```php
public string $server_key_public_exponent
```

Logged for debug purposes



**See Also:**

* \phpseclib\Net\self::getServerKeyPublicExponent() - 

***

### server_key_public_modulus

The Server Key Public Modulus

```php
public string $server_key_public_modulus
```

Logged for debug purposes



**See Also:**

* \phpseclib\Net\self::getServerKeyPublicModulus() - 

***

### host_key_public_exponent

The Host Key Public Exponent

```php
public string $host_key_public_exponent
```

Logged for debug purposes



**See Also:**

* \phpseclib\Net\self::getHostKeyPublicExponent() - 

***

### host_key_public_modulus

The Host Key Public Modulus

```php
public string $host_key_public_modulus
```

Logged for debug purposes



**See Also:**

* \phpseclib\Net\self::getHostKeyPublicModulus() - 

***

### supported_ciphers

Supported Ciphers

```php
public array $supported_ciphers
```

Logged for debug purposes



**See Also:**

* \phpseclib\Net\self::getSupportedCiphers() - 

***

### supported_authentications

Supported Authentications

```php
public array $supported_authentications
```

Logged for debug purposes



**See Also:**

* \phpseclib\Net\self::getSupportedAuthentications() - 

***

### server_identification

Server Identification

```php
public string $server_identification
```





**See Also:**

* \phpseclib\Net\self::getServerIdentification() - 

***

### protocol_flags

Protocol Flags

```php
public array $protocol_flags
```





**See Also:**

* \phpseclib\Net\self::__construct() - 

***

### protocol_flags_log

Protocol Flag Log

```php
public array $protocol_flags_log
```





**See Also:**

* \phpseclib\Net\self::getLog() - 

***

### message_log

Message Log

```php
public array $message_log
```





**See Also:**

* \phpseclib\Net\self::getLog() - 

***

### realtime_log_file

Real-time log file pointer

```php
public resource $realtime_log_file
```





**See Also:**

* \phpseclib\Net\self::_append_log() - 

***

### realtime_log_size

Real-time log file size

```php
public int $realtime_log_size
```





**See Also:**

* \phpseclib\Net\self::_append_log() - 

***

### realtime_log_wrap

Real-time log file wrap boolean

```php
public bool $realtime_log_wrap
```





**See Also:**

* \phpseclib\Net\self::_append_log() - 

***

### interactiveBuffer

Interactive Buffer

```php
public array $interactiveBuffer
```





**See Also:**

* \phpseclib\Net\self::read() - 

***

### log_size

Current log size

```php
public int $log_size
```

Should never exceed self::LOG_MAX_SIZE



**See Also:**

* \phpseclib\Net\self::_send_binary_packet() - * \phpseclib\Net\self::_get_binary_packet() - 

***

### timeout

Timeout

```php
public $timeout
```





**See Also:**

* \phpseclib\Net\self::setTimeout() - 

***

### curTimeout

Current Timeout

```php
public $curTimeout
```





**See Also:**

* \phpseclib\Net\self::_get_channel_packet() - 

***

### log_boundary

Log Boundary

```php
public $log_boundary
```





**See Also:**

* \phpseclib\Net\self::_format_log() - 

***

### log_long_width

Log Long Width

```php
public $log_long_width
```





**See Also:**

* \phpseclib\Net\self::_format_log() - 

***

### log_short_width

Log Short Width

```php
public $log_short_width
```





**See Also:**

* \phpseclib\Net\self::_format_log() - 

***

### host

Hostname

```php
public string $host
```





**See Also:**

* \phpseclib\Net\self::__construct() - * \phpseclib\Net\self::_connect() - 

***

### port

Port Number

```php
public int $port
```





**See Also:**

* \phpseclib\Net\self::__construct() - * \phpseclib\Net\self::_connect() - 

***

### connectionTimeout

Timeout for initial connection

```php
public int $connectionTimeout
```

Set by the constructor call. Calling setTimeout() is optional. If it's not called functions like
exec() won't timeout unless some PHP setting forces it too. The timeout specified in the constructor,
however, is non-optional. There will be a timeout, whether or not you set it. If you don't it'll be
10 seconds. It is used by fsockopen() in that function.



**See Also:**

* \phpseclib\Net\self::__construct() - * \phpseclib\Net\self::_connect() - 

***

### cipher

Default cipher

```php
public int $cipher
```





**See Also:**

* \phpseclib\Net\self::__construct() - * \phpseclib\Net\self::_connect() - 

***

## Methods


### __construct

Default Constructor.

```php
public __construct(string $host, int $port = 22, int $timeout = 10, int $cipher = self::CIPHER_3DES): \phpseclib\Net\SSH1
```

Connects to an SSHv1 server






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$host` | **string** |  |
| `$port` | **int** |  |
| `$timeout` | **int** |  |
| `$cipher` | **int** |  |





***

### _connect

Connect to an SSHv1 server

```php
public _connect(): bool
```












***

### login

Login

```php
public login(string $username, string $password = &#039;&#039;): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$username` | **string** |  |
| `$password` | **string** |  |





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

### exec

Executes a command on a non-interactive shell, returns the output, and quits.

```php
public exec(string $cmd, bool $block = true): mixed
```

An SSH1 server will close the connection after a command has been executed on a non-interactive shell.  SSH2
servers don't, however, this isn't an SSH2 client.  The way this works, on the server, is by initiating a
shell with the -s option, as discussed in the following links:

{@link http://www.faqs.org/docs/bashman/bashref_65.html}
{@link http://www.faqs.org/docs/bashman/bashref_62.html}

To execute further commands, a new \phpseclib\Net\SSH1 object will need to be created.

Returns false on failure and the output, otherwise.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cmd` | **string** |  |
| `$block` | **bool** |  |





**See Also:**

* \phpseclib\Net\self::interactiveRead() - * \phpseclib\Net\self::interactiveWrite() - 

***

### _initShell

Creates an interactive shell

```php
public _initShell(): bool
```












**See Also:**

* \phpseclib\Net\self::interactiveRead() - * \phpseclib\Net\self::interactiveWrite() - 

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

* \phpseclib\Net\self::interactiveWrite() - 

***

### read

Returns the output of an interactive shell when there's a match for $expect

```php
public read(string $expect, int $mode = self::READ_SIMPLE): bool
```

$expect can take the form of a string literal or, if $mode == self::READ_REGEX,
a regular expression.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$expect` | **string** |  |
| `$mode` | **int** |  |





**See Also:**

* \phpseclib\Net\self::write() - 

***

### interactiveWrite

Inputs a command into an interactive shell.

```php
public interactiveWrite(string $cmd): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cmd` | **string** |  |





**See Also:**

* \phpseclib\Net\self::interactiveRead() - 

***

### interactiveRead

Returns the output of an interactive shell when no more output is available.

```php
public interactiveRead(): string
```

Requires PHP 4.3.0 or later due to the use of the stream_select() function.  If you see stuff like
"^[[00m", you're seeing ANSI escape codes.  According to
{@link http://support.microsoft.com/kb/101875}, "Windows NT
does not support ANSI escape sequences in Win32 Console applications", so if you're a Windows user,
there's not going to be much recourse.










**See Also:**

* \phpseclib\Net\self::interactiveRead() - 

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

### _disconnect

Disconnect

```php
public _disconnect(string $msg = &#039;Client Quit&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$msg` | **string** |  |





***

### _get_binary_packet

Gets Binary Packets

```php
public _get_binary_packet(): array
```

See 'The Binary Packet Protocol' of protocol-1.5.txt for more info.

Also, this function could be improved upon by adding detection for the following exploit:
http://www.securiteam.com/securitynews/5LP042K3FY.html










**See Also:**

* \phpseclib\Net\self::_send_binary_packet() - 

***

### _send_binary_packet

Sends Binary Packets

```php
public _send_binary_packet(string $data): bool
```

Returns true on success, false on failure.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





**See Also:**

* \phpseclib\Net\self::_get_binary_packet() - 

***

### _crc

Cyclic Redundancy Check (CRC)

```php
public _crc(string $data): int
```

PHP's crc32 function is implemented slightly differently than the one that SSH v1 uses, so
we've reimplemented it. A more detailed discussion of the differences can be found after
$crc_lookup_table's initialization.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |





**See Also:**

* \phpseclib\Net\self::_get_binary_packet() - * \phpseclib\Net\self::_send_binary_packet() - 

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

### _rsa_crypt

RSA Encrypt

```php
public _rsa_crypt(\phpseclib\Math\BigInteger $m, array $key): \phpseclib\Math\BigInteger
```

Returns mod(pow($m, $e), $n), where $n should be the product of two (large) primes $p and $q and where $e
should be a number with the property that gcd($e, ($p - 1) * ($q - 1)) == 1.  Could just make anything that
calls this call modexp, instead, but I think this makes things clearer, maybe...






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m` | **\phpseclib\Math\BigInteger** |  |
| `$key` | **array** |  |





**See Also:**

* \phpseclib\Net\self::__construct() - 

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

Returns a string if NET_SSH1_LOGGING == self::LOG_COMPLEX, an array if NET_SSH1_LOGGING == self::LOG_SIMPLE and false if !defined('NET_SSH1_LOGGING')










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

### getServerKeyPublicExponent

Return the server key public exponent

```php
public getServerKeyPublicExponent(bool $raw_output = false): string
```

Returns, by default, the base-10 representation.  If $raw_output is set to true, returns, instead,
the raw bytes.  This behavior is similar to PHP's md5() function.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$raw_output` | **bool** |  |





***

### getServerKeyPublicModulus

Return the server key public modulus

```php
public getServerKeyPublicModulus(bool $raw_output = false): string
```

Returns, by default, the base-10 representation.  If $raw_output is set to true, returns, instead,
the raw bytes.  This behavior is similar to PHP's md5() function.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$raw_output` | **bool** |  |





***

### getHostKeyPublicExponent

Return the host key public exponent

```php
public getHostKeyPublicExponent(bool $raw_output = false): string
```

Returns, by default, the base-10 representation.  If $raw_output is set to true, returns, instead,
the raw bytes.  This behavior is similar to PHP's md5() function.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$raw_output` | **bool** |  |





***

### getHostKeyPublicModulus

Return the host key public modulus

```php
public getHostKeyPublicModulus(bool $raw_output = false): string
```

Returns, by default, the base-10 representation.  If $raw_output is set to true, returns, instead,
the raw bytes.  This behavior is similar to PHP's md5() function.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$raw_output` | **bool** |  |





***

### getSupportedCiphers

Return a list of ciphers supported by SSH1 server.

```php
public getSupportedCiphers(bool $raw_output = false): array
```

Just because a cipher is supported by an SSH1 server doesn't mean it's supported by this library. If $raw_output
is set to true, returns, instead, an array of constants.  ie. instead of array('Triple-DES in CBC mode'), you'll
get array(self::CIPHER_3DES).






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$raw_output` | **bool** |  |





***

### getSupportedAuthentications

Return a list of authentications supported by SSH1 server.

```php
public getSupportedAuthentications(bool $raw_output = false): array
```

Just because a cipher is supported by an SSH1 server doesn't mean it's supported by this library. If $raw_output
is set to true, returns, instead, an array of constants.  ie. instead of array('password authentication'), you'll
get array(self::AUTH_PASSWORD).






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$raw_output` | **bool** |  |





***

### getServerIdentification

Return the server identification.

```php
public getServerIdentification(): string
```












***

### _append_log

Logs data packets

```php
public _append_log(int $protocol_flags, string $message): mixed
```

Makes sure that only the last 1MB worth of packets will be logged






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$protocol_flags` | **int** |  |
| `$message` | **string** |  |





***


***
> Automatically generated on 2025-03-15
