
# SSH2

Pure-PHP implementation of SSHv2.



* Full name: `\phpseclib\Net\SSH2`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`NET_SSH2_COMPRESSION_NONE`|public| |1|
|`NET_SSH2_COMPRESSION_ZLIB`|public| |2|
|`NET_SSH2_COMPRESSION_ZLIB_AT_OPENSSH`|public| |3|
|`MASK_CONSTRUCTOR`|public| |0x1|
|`MASK_CONNECTED`|public| |0x2|
|`MASK_LOGIN_REQ`|public| |0x4|
|`MASK_LOGIN`|public| |0x8|
|`MASK_SHELL`|public| |0x10|
|`MASK_WINDOW_ADJUST`|public| |0x20|
|`CHANNEL_EXEC`|public| |1|
|`CHANNEL_SHELL`|public| |2|
|`CHANNEL_SUBSYSTEM`|public| |3|
|`CHANNEL_AGENT_FORWARD`|public| |4|
|`CHANNEL_KEEP_ALIVE`|public| |5|
|`LOG_SIMPLE`|public| |1|
|`LOG_COMPLEX`|public| |2|
|`LOG_REALTIME`|public| |3|
|`LOG_REALTIME_FILE`|public| |4|
|`LOG_MAX_SIZE`|public| |1048576|
|`READ_SIMPLE`|public| |1|
|`READ_REGEX`|public| |2|
|`READ_NEXT`|public| |3|

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

### bitmap

Execution Bitmap

```php
public int $bitmap
```

The bits that are set represent functions that have been called already.  This is used to determine
if a requisite function has been successfully executed.  If not, an error should be thrown.




***

### errors

Error information

```php
public string $errors
```





**See Also:**

* \phpseclib\Net\self::getErrors() - * \phpseclib\Net\self::getLastError() - 

***

### server_identifier

Server Identifier

```php
public array|false $server_identifier
```





**See Also:**

* \phpseclib\Net\self::getServerIdentification() - 

***

### kex_algorithms

Key Exchange Algorithms

```php
public array|false $kex_algorithms
```





**See Also:**

* \phpseclib\Net\self::getKexAlgorithims() - 

***

### kex_algorithm

Key Exchange Algorithm

```php
public string|false $kex_algorithm
```





**See Also:**

* \phpseclib\Net\self::getMethodsNegotiated() - 

***

### kex_dh_group_size_min

Minimum Diffie-Hellman Group Bit Size in RFC 4419 Key Exchange Methods

```php
public int $kex_dh_group_size_min
```





**See Also:**

* \phpseclib\Net\self::_key_exchange() - 

***

### kex_dh_group_size_preferred

Preferred Diffie-Hellman Group Bit Size in RFC 4419 Key Exchange Methods

```php
public int $kex_dh_group_size_preferred
```





**See Also:**

* \phpseclib\Net\self::_key_exchange() - 

***

### kex_dh_group_size_max

Maximum Diffie-Hellman Group Bit Size in RFC 4419 Key Exchange Methods

```php
public int $kex_dh_group_size_max
```





**See Also:**

* \phpseclib\Net\self::_key_exchange() - 

***

### server_host_key_algorithms

Server Host Key Algorithms

```php
public array|false $server_host_key_algorithms
```





**See Also:**

* \phpseclib\Net\self::getServerHostKeyAlgorithms() - 

***

### supported_private_key_algorithms

Supported Private Key Algorithms

```php
public array|false $supported_private_key_algorithms
```

In theory this should be the same as the Server Host Key Algorithms but, in practice,
some servers (eg. Azure) will support rsa-sha2-512 as a server host key algorithm but
not a private key algorithm



**See Also:**

* \phpseclib\Net\self::privatekey_login() - 

***

### encryption_algorithms_client_to_server

Encryption Algorithms: Client to Server

```php
public array|false $encryption_algorithms_client_to_server
```





**See Also:**

* \phpseclib\Net\self::getEncryptionAlgorithmsClient2Server() - 

***

### encryption_algorithms_server_to_client

Encryption Algorithms: Server to Client

```php
public array|false $encryption_algorithms_server_to_client
```





**See Also:**

* \phpseclib\Net\self::getEncryptionAlgorithmsServer2Client() - 

***

### mac_algorithms_client_to_server

MAC Algorithms: Client to Server

```php
public array|false $mac_algorithms_client_to_server
```





**See Also:**

* \phpseclib\Net\self::getMACAlgorithmsClient2Server() - 

***

### mac_algorithms_server_to_client

MAC Algorithms: Server to Client

```php
public array|false $mac_algorithms_server_to_client
```





**See Also:**

* \phpseclib\Net\self::getMACAlgorithmsServer2Client() - 

***

### compression_algorithms_client_to_server

Compression Algorithms: Client to Server

```php
public array|false $compression_algorithms_client_to_server
```





**See Also:**

* \phpseclib\Net\self::getCompressionAlgorithmsClient2Server() - 

***

### compression_algorithms_server_to_client

Compression Algorithms: Server to Client

```php
public array|false $compression_algorithms_server_to_client
```





**See Also:**

* \phpseclib\Net\self::getCompressionAlgorithmsServer2Client() - 

***

### languages_server_to_client

Languages: Server to Client

```php
public array|false $languages_server_to_client
```





**See Also:**

* \phpseclib\Net\self::getLanguagesServer2Client() - 

***

### languages_client_to_server

Languages: Client to Server

```php
public array|false $languages_client_to_server
```





**See Also:**

* \phpseclib\Net\self::getLanguagesClient2Server() - 

***

### preferred

Preferred Algorithms

```php
public array $preferred
```





**See Also:**

* \phpseclib\Net\self::setPreferredAlgorithms() - 

***

### encrypt_block_size

Block Size for Server to Client Encryption

```php
public int $encrypt_block_size
```

"Note that the length of the concatenation of 'packet_length',
'padding_length', 'payload', and 'random padding' MUST be a multiple
of the cipher block size or 8, whichever is larger.  This constraint
MUST be enforced, even when using stream ciphers."

-- http://tools.ietf.org/html/rfc4253#section-6



**See Also:**

* \phpseclib\Net\self::__construct() - * \phpseclib\Net\self::_send_binary_packet() - 

***

### decrypt_block_size

Block Size for Client to Server Encryption

```php
public int $decrypt_block_size
```





**See Also:**

* \phpseclib\Net\self::__construct() - * \phpseclib\Net\self::_get_binary_packet() - 

***

### decrypt

Server to Client Encryption Object

```php
public object $decrypt
```





**See Also:**

* \phpseclib\Net\self::_get_binary_packet() - 

***

### decryptName

Decryption Algorithm Name

```php
public string|null $decryptName
```






***

### encrypt

Client to Server Encryption Object

```php
public object $encrypt
```





**See Also:**

* \phpseclib\Net\self::_send_binary_packet() - 

***

### encryptName

Encryption Algorithm Name

```php
public string|null $encryptName
```






***

### hmac_create

Client to Server HMAC Object

```php
public object $hmac_create
```





**See Also:**

* \phpseclib\Net\self::_send_binary_packet() - 

***

### hmac_create_name

Client to Server HMAC Name

```php
private string|false $hmac_create_name
```






***

### hmac_check

Server to Client HMAC Object

```php
public object $hmac_check
```





**See Also:**

* \phpseclib\Net\self::_get_binary_packet() - 

***

### hmac_check_name

Server to Client HMAC Name

```php
public string|false $hmac_check_name
```






***

### hmac_size

Size of server to client HMAC

```php
public int $hmac_size
```

We need to know how big the HMAC will be for the server to client direction so that we know how many bytes to read.
For the client to server side, the HMAC object will make the HMAC as long as it needs to be.  All we need to do is
append it.



**See Also:**

* \phpseclib\Net\self::_get_binary_packet() - 

***

### server_public_host_key

Server Public Host Key

```php
public string $server_public_host_key
```





**See Also:**

* \phpseclib\Net\self::getServerPublicHostKey() - 

***

### session_id

Session identifier

```php
public string $session_id
```

"The exchange hash H from the first key exchange is additionally
used as the session identifier, which is a unique identifier for
this connection."

-- http://tools.ietf.org/html/rfc4253#section-7.2



**See Also:**

* \phpseclib\Net\self::_key_exchange() - 

***

### exchange_hash

Exchange hash

```php
public string $exchange_hash
```

The current exchange hash



**See Also:**

* \phpseclib\Net\self::_key_exchange() - 

***

### message_numbers

Message Numbers

```php
public array $message_numbers
```





**See Also:**

* \phpseclib\Net\self::__construct() - 

***

### disconnect_reasons

Disconnection Message 'reason codes' defined in RFC4253

```php
public array $disconnect_reasons
```





**See Also:**

* \phpseclib\Net\self::__construct() - 

***

### channel_open_failure_reasons

SSH_MSG_CHANNEL_OPEN_FAILURE 'reason codes', defined in RFC4254

```php
public array $channel_open_failure_reasons
```





**See Also:**

* \phpseclib\Net\self::__construct() - 

***

### terminal_modes

Terminal Modes

```php
public array $terminal_modes
```





**See Also:**

* \phpseclib\Net\self::__construct() - * http://tools.ietf.org/html/rfc4254#section-8 - 

***

### channel_extended_data_type_codes

SSH_MSG_CHANNEL_EXTENDED_DATA's data_type_codes

```php
public array $channel_extended_data_type_codes
```





**See Also:**

* \phpseclib\Net\self::__construct() - * http://tools.ietf.org/html/rfc4254#section-5.2 - 

***

### send_seq_no

Send Sequence Number

```php
public int $send_seq_no
```

See 'Section 6.4.  Data Integrity' of rfc4253 for more info.



**See Also:**

* \phpseclib\Net\self::_send_binary_packet() - 

***

### get_seq_no

Get Sequence Number

```php
public int $get_seq_no
```

See 'Section 6.4.  Data Integrity' of rfc4253 for more info.



**See Also:**

* \phpseclib\Net\self::_get_binary_packet() - 

***

### server_channels

Server Channels

```php
public array $server_channels
```

Maps client channels to server channels



**See Also:**

* \phpseclib\Net\self::_get_channel_packet() - * \phpseclib\Net\self::exec() - 

***

### channel_buffers

Channel Buffers

```php
public array $channel_buffers
```

If a client requests a packet from one channel but receives two packets from another those packets should
be placed in a buffer



**See Also:**

* \phpseclib\Net\self::_get_channel_packet() - * \phpseclib\Net\self::exec() - 

***

### channel_status

Channel Status

```php
public array $channel_status
```

Contains the type of the last sent message



**See Also:**

* \phpseclib\Net\self::_get_channel_packet() - 

***

### packet_size_client_to_server

Packet Size

```php
public array $packet_size_client_to_server
```

Maximum packet size indexed by channel



**See Also:**

* \phpseclib\Net\self::_send_channel_packet() - 

***

### message_number_log

Message Number Log

```php
public array $message_number_log
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

### window_size

The Window Size

```php
public int $window_size
```

Bytes the other party can send before it must wait for the window to be adjusted (0x7FFFFFFF = 2GB)



**See Also:**

* \phpseclib\Net\self::_send_channel_packet() - * \phpseclib\Net\self::exec() - 

***

### window_resize

What we resize the window to

```php
public int $window_resize
```

When PuTTY resizes the window it doesn't add an additional 0x7FFFFFFF bytes - it adds 0x40000000 bytes.
Some SFTP clients (GoAnywhere) don't support adding 0x7FFFFFFF to the window size after the fact so
we'll just do what PuTTY does



**See Also:**

* \phpseclib\Net\self::_send_channel_packet() - * \phpseclib\Net\self::exec() - 

***

### window_size_server_to_client

Window size, server to client

```php
public array $window_size_server_to_client
```

Window size indexed by channel



**See Also:**

* \phpseclib\Net\self::_send_channel_packet() - 

***

### window_size_client_to_server

Window size, client to server

```php
public array $window_size_client_to_server
```

Window size indexed by channel



**See Also:**

* \phpseclib\Net\self::_get_channel_packet() - 

***

### signature

Server signature

```php
public string $signature
```

Verified against $this->session_id



**See Also:**

* \phpseclib\Net\self::getServerPublicHostKey() - 

***

### signature_format

Server signature format

```php
public string $signature_format
```

ssh-rsa or ssh-dss.



**See Also:**

* \phpseclib\Net\self::getServerPublicHostKey() - 

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

### keepAlive

Keep Alive Interval

```php
public $keepAlive
```





**See Also:**

* \phpseclib\Net\self::setKeepAlive() - 

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

### signature_validated

Has the signature been validated?

```php
public bool $signature_validated
```





**See Also:**

* \phpseclib\Net\self::getServerPublicHostKey() - 

***

### realtime_log_wrap

Real-time log file wrap boolean

```php
public $realtime_log_wrap
```





**See Also:**

* \phpseclib\Net\self::_append_log() - 

***

### quiet_mode

Flag to suppress stderr from output

```php
public $quiet_mode
```





**See Also:**

* \phpseclib\Net\self::enableQuietMode() - 

***

### last_packet

Time of first network activity

```php
public int $last_packet
```






***

### exit_status

Exit status returned from ssh if any

```php
public int $exit_status
```






***

### request_pty

Flag to request a PTY when using exec()

```php
public bool $request_pty
```





**See Also:**

* \phpseclib\Net\self::enablePTY() - 

***

### in_request_pty_exec

Flag set while exec() is running when using enablePTY()

```php
public bool $in_request_pty_exec
```






***

### in_subsystem

Flag set after startSubsystem() is called

```php
public bool $in_subsystem
```






***

### stdErrorLog

Contents of stdError

```php
public string $stdErrorLog
```






***

### last_interactive_response

The Last Interactive Response

```php
public string $last_interactive_response
```





**See Also:**

* \phpseclib\Net\self::_keyboard_interactive_process() - 

***

### keyboard_requests_responses

Keyboard Interactive Request / Responses

```php
public array $keyboard_requests_responses
```





**See Also:**

* \phpseclib\Net\self::_keyboard_interactive_process() - 

***

### banner_message

Banner Message

```php
public string $banner_message
```

Quoting from the RFC, "in some jurisdictions, sending a warning message before
authentication may be relevant for getting legal protection."



**See Also:**

* \phpseclib\Net\self::_filter() - * \phpseclib\Net\self::getBannerMessage() - 

***

### is_timeout

Did read() timeout or return normally?

```php
public bool $is_timeout
```





**See Also:**

* \phpseclib\Net\self::isTimeout() - 

***

### log_boundary

Log Boundary

```php
public string $log_boundary
```





**See Also:**

* \phpseclib\Net\self::_format_log() - 

***

### log_long_width

Log Long Width

```php
public int $log_long_width
```





**See Also:**

* \phpseclib\Net\self::_format_log() - 

***

### log_short_width

Log Short Width

```php
public int $log_short_width
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

### windowColumns

Number of columns for terminal window size

```php
public int $windowColumns
```





**See Also:**

* \phpseclib\Net\self::getWindowColumns() - * \phpseclib\Net\self::setWindowColumns() - * \phpseclib\Net\self::setWindowSize() - 

***

### windowRows

Number of columns for terminal window size

```php
public int $windowRows
```





**See Also:**

* \phpseclib\Net\self::getWindowRows() - * \phpseclib\Net\self::setWindowRows() - * \phpseclib\Net\self::setWindowSize() - 

***

### crypto_engine

Crypto Engine

```php
public int $crypto_engine
```





**See Also:**

* \phpseclib\Net\self::setCryptoEngine() - * \phpseclib\Net\self::_key_exchange() - 

***

### agent

A System_SSH_Agent for use in the SSH2 Agent Forwarding scenario

```php
public \phpseclib\Net\System_SSH_Agent $agent
```






***

### send_id_string_first

Send the identification string first?

```php
public bool $send_id_string_first
```






***

### send_kex_first

Send the key exchange initiation packet first?

```php
public bool $send_kex_first
```






***

### bad_key_size_fix

Some versions of OpenSSH incorrectly calculate the key size

```php
public bool $bad_key_size_fix
```






***

### retry_connect

Should we try to re-connect to re-establish keys?

```php
public bool $retry_connect
```






***

### binary_packet_buffer

Binary Packet Buffer

```php
public string|false $binary_packet_buffer
```






***

### preferred_signature_format

Preferred Signature Format

```php
public string|false $preferred_signature_format
```






***

### auth

Authentication Credentials

```php
public array $auth
```






***

### auth_methods_to_continue

The authentication methods that may productively continue authentication.

```php
public array|null $auth_methods_to_continue
```





**See Also:**

* https://tools.ietf.org/html/rfc4252#section-5.1 - 

***

### compress

Compression method

```php
public int $compress
```






***

### decompress

Decompression method

```php
public resource|object $decompress
```






***

### compress_context

Compression context

```php
public int $compress_context
```






***

### decompress_context

Decompression context

```php
public resource|object $decompress_context
```






***

### regenerate_compression_context

Regenerate Compression Context

```php
public bool $regenerate_compression_context
```






***

### regenerate_decompression_context

Regenerate Decompression Context

```php
public bool $regenerate_decompression_context
```






***

### smartMFA

Smart multi-factor authentication flag

```php
public bool $smartMFA
```






***

### extra_packets

Extra packets counter

```php
public bool $extra_packets
```






***

## Methods


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
> Automatically generated on 2025-03-18
