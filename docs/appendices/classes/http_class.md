
# http_class





* Full name: `\http_class`



## Properties


### host_name



```php
public $host_name
```






***

### host_port



```php
public $host_port
```






***

### proxy_host_name



```php
public $proxy_host_name
```






***

### proxy_host_port



```php
public $proxy_host_port
```






***

### socks_host_name



```php
public $socks_host_name
```






***

### socks_host_port



```php
public $socks_host_port
```






***

### socks_version



```php
public $socks_version
```






***

### protocol



```php
public $protocol
```






***

### request_method



```php
public $request_method
```






***

### user_agent



```php
public $user_agent
```






***

### accept



```php
public $accept
```






***

### authentication_mechanism



```php
public $authentication_mechanism
```






***

### user



```php
public $user
```






***

### password



```php
public $password
```






***

### realm



```php
public $realm
```






***

### workstation



```php
public $workstation
```






***

### proxy_authentication_mechanism



```php
public $proxy_authentication_mechanism
```






***

### proxy_user



```php
public $proxy_user
```






***

### proxy_password



```php
public $proxy_password
```






***

### proxy_realm



```php
public $proxy_realm
```






***

### proxy_workstation



```php
public $proxy_workstation
```






***

### request_uri



```php
public $request_uri
```






***

### request



```php
public $request
```






***

### request_headers



```php
public $request_headers
```






***

### request_user



```php
public $request_user
```






***

### request_password



```php
public $request_password
```






***

### request_realm



```php
public $request_realm
```






***

### request_workstation



```php
public $request_workstation
```






***

### proxy_request_user



```php
public $proxy_request_user
```






***

### proxy_request_password



```php
public $proxy_request_password
```






***

### proxy_request_realm



```php
public $proxy_request_realm
```






***

### proxy_request_workstation



```php
public $proxy_request_workstation
```






***

### request_body



```php
public $request_body
```






***

### request_arguments



```php
public $request_arguments
```






***

### protocol_version



```php
public $protocol_version
```






***

### timeout



```php
public $timeout
```






***

### data_timeout



```php
public $data_timeout
```






***

### debug



```php
public $debug
```






***

### log_debug



```php
public $log_debug
```






***

### debug_response_body



```php
public $debug_response_body
```






***

### html_debug



```php
public $html_debug
```






***

### support_cookies



```php
public $support_cookies
```






***

### cookies



```php
public $cookies
```






***

### error



```php
public $error
```






***

### error_code



```php
public $error_code
```






***

### exclude_address



```php
public $exclude_address
```






***

### follow_redirect



```php
public $follow_redirect
```






***

### redirection_limit



```php
public $redirection_limit
```






***

### response_status



```php
public $response_status
```






***

### response_message



```php
public $response_message
```






***

### file_buffer_length



```php
public $file_buffer_length
```






***

### force_multipart_form_post



```php
public $force_multipart_form_post
```






***

### prefer_curl



```php
public $prefer_curl
```






***

### keep_alive



```php
public $keep_alive
```






***

### sasl_authenticate



```php
public $sasl_authenticate
```






***

### state



```php
public $state
```






***

### use_curl



```php
public $use_curl
```






***

### connection



```php
public $connection
```






***

### content_length



```php
public $content_length
```






***

### response



```php
public $response
```






***

### read_response



```php
public $read_response
```






***

### read_length



```php
public $read_length
```






***

### request_host



```php
public $request_host
```






***

### next_token



```php
public $next_token
```






***

### redirection_level



```php
public $redirection_level
```






***

### chunked



```php
public $chunked
```






***

### remaining_chunk



```php
public $remaining_chunk
```






***

### last_chunk_read



```php
public $last_chunk_read
```






***

### months



```php
public $months
```






***

### session



```php
public $session
```






***

### connection_close



```php
public $connection_close
```






***

### force_close



```php
public $force_close
```






***

### connected_host



```php
public $connected_host
```






***

### connected_port



```php
public $connected_port
```






***

### connected_ssl



```php
public $connected_ssl
```






***

## Methods


### Tokenize



```php
public Tokenize(mixed $string, mixed $separator = &quot;&quot;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **mixed** |  |
| `$separator` | **mixed** |  |





***

### CookieEncode



```php
public CookieEncode(mixed $value, mixed $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **mixed** |  |
| `$name` | **mixed** |  |





***

### SetError



```php
public SetError(mixed $error, mixed $error_code = HTTP_CLIENT_ERROR_UNSPECIFIED_ERROR): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$error` | **mixed** |  |
| `$error_code` | **mixed** |  |





***

### SetPHPError



```php
public SetPHPError(mixed $error, mixed& $php_error_message, mixed $error_code = HTTP_CLIENT_ERROR_UNSPECIFIED_ERROR): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$error` | **mixed** |  |
| `$php_error_message` | **mixed** |  |
| `$error_code` | **mixed** |  |





***

### SetDataAccessError



```php
public SetDataAccessError(mixed $error, mixed $check_connection): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$error` | **mixed** |  |
| `$check_connection` | **mixed** |  |





***

### OutputDebug



```php
public OutputDebug(mixed $message): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$message` | **mixed** |  |





***

### GetLine



```php
public GetLine(): mixed
```












***

### PutLine



```php
public PutLine(mixed $line): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$line` | **mixed** |  |





***

### PutData



```php
public PutData(mixed $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |





***

### FlushData



```php
public FlushData(): mixed
```












***

### ReadChunkSize



```php
public ReadChunkSize(): mixed
```












***

### ReadBytes



```php
public ReadBytes(mixed $length): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$length` | **mixed** |  |





***

### EndOfInput



```php
public EndOfInput(): mixed
```












***

### Resolve



```php
public Resolve(mixed $domain, mixed& $ip, mixed $server_type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$domain` | **mixed** |  |
| `$ip` | **mixed** |  |
| `$server_type` | **mixed** |  |





***

### Connect



```php
public Connect(mixed $host_name, mixed $host_port, mixed $ssl, mixed $server_type = &#039;HTTP&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$host_name` | **mixed** |  |
| `$host_port` | **mixed** |  |
| `$ssl` | **mixed** |  |
| `$server_type` | **mixed** |  |





***

### Disconnect



```php
public Disconnect(): mixed
```












***

### GetRequestArguments



```php
public GetRequestArguments(mixed $url, mixed& $arguments): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |
| `$arguments` | **mixed** |  |





***

### Open



```php
public Open(mixed $arguments): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arguments` | **mixed** |  |





***

### Close



```php
public Close(mixed $force): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$force` | **mixed** |  |





***

### PickCookies



```php
public PickCookies(mixed& $cookies, mixed $secure): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cookies` | **mixed** |  |
| `$secure` | **mixed** |  |





***

### GetFileDefinition



```php
public GetFileDefinition(mixed $file, mixed& $definition): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **mixed** |  |
| `$definition` | **mixed** |  |





***

### ConnectFromProxy



```php
public ConnectFromProxy(mixed $arguments, mixed& $headers): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arguments` | **mixed** |  |
| `$headers` | **mixed** |  |





***

### SendRequest



```php
public SendRequest(mixed $arguments): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arguments` | **mixed** |  |





***

### SetCookie



```php
public SetCookie(mixed $name, mixed $value, mixed $expires = &quot;&quot;, mixed $path = &quot;/&quot;, mixed $domain = &quot;&quot;, mixed $secure, mixed $verbatim): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |
| `$value` | **mixed** |  |
| `$expires` | **mixed** |  |
| `$path` | **mixed** |  |
| `$domain` | **mixed** |  |
| `$secure` | **mixed** |  |
| `$verbatim` | **mixed** |  |





***

### SendRequestBody



```php
public SendRequestBody(mixed $data, mixed $end_of_data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$end_of_data` | **mixed** |  |





***

### ReadReplyHeadersResponse



```php
public ReadReplyHeadersResponse(mixed& $headers): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$headers` | **mixed** |  |





***

### Redirect



```php
public Redirect(mixed& $headers): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$headers` | **mixed** |  |





***

### Authenticate



```php
public Authenticate(mixed& $headers, mixed $proxy, mixed& $proxy_authorization, mixed& $user, mixed& $password, mixed& $realm, mixed& $workstation): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$headers` | **mixed** |  |
| `$proxy` | **mixed** |  |
| `$proxy_authorization` | **mixed** |  |
| `$user` | **mixed** |  |
| `$password` | **mixed** |  |
| `$realm` | **mixed** |  |
| `$workstation` | **mixed** |  |





***

### ReadReplyHeaders



```php
public ReadReplyHeaders(mixed& $headers): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$headers` | **mixed** |  |





***

### ReadReplyBody



```php
public ReadReplyBody(mixed& $body, mixed $length): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$body` | **mixed** |  |
| `$length` | **mixed** |  |





***

### ReadWholeReplyBody



```php
public ReadWholeReplyBody(mixed& $body): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$body` | **mixed** |  |





***

### SaveCookies



```php
public SaveCookies(mixed& $cookies, mixed $domain = &#039;&#039;, mixed $secure_only, mixed $persistent_only): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cookies` | **mixed** |  |
| `$domain` | **mixed** |  |
| `$secure_only` | **mixed** |  |
| `$persistent_only` | **mixed** |  |





***

### SavePersistentCookies



```php
public SavePersistentCookies(mixed& $cookies, mixed $domain = &#039;&#039;, mixed $secure_only): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cookies` | **mixed** |  |
| `$domain` | **mixed** |  |
| `$secure_only` | **mixed** |  |





***

### GetPersistentCookies



```php
public GetPersistentCookies(mixed& $cookies, mixed $domain = &#039;&#039;, mixed $secure_only): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cookies` | **mixed** |  |
| `$domain` | **mixed** |  |
| `$secure_only` | **mixed** |  |





***

### RestoreCookies



```php
public RestoreCookies(mixed $cookies, mixed $clear = 1): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cookies` | **mixed** |  |
| `$clear` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
