
# OAuth2





* Full name: `\OAuth2`
* This class is an **Abstract class**



## Properties


### access_token_lifetime



```php
private $access_token_lifetime
```






***

### auth_code_lifetime



```php
private $auth_code_lifetime
```






***

### refresh_token_lifetime



```php
private $refresh_token_lifetime
```






***

## Methods


### auth_client_credentials



```php
protected auth_client_credentials(mixed $client_id, mixed $client_secret = null): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$client_secret` | **mixed** |  |





***

### get_redirect_uri



```php
protected get_redirect_uri(mixed $client_id): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***

### get_access_token



```php
protected get_access_token(mixed $token_id): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token_id` | **mixed** |  |





***

### store_access_token



```php
protected store_access_token(mixed $token_id, mixed $client_id, mixed $expires, mixed $scope = null): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token_id` | **mixed** |  |
| `$client_id` | **mixed** |  |
| `$expires` | **mixed** |  |
| `$scope` | **mixed** |  |





***

### get_supported_grant_types



```php
protected get_supported_grant_types(): mixed
```












***

### get_supported_auth_response_types



```php
protected get_supported_auth_response_types(): mixed
```












***

### get_supported_scopes



```php
protected get_supported_scopes(): mixed
```












***

### authorize_client_response_type



```php
protected authorize_client_response_type(mixed $client_id, mixed $response_type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$response_type` | **mixed** |  |





***

### authorize_client



```php
protected authorize_client(mixed $client_id, mixed $grant_type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$grant_type` | **mixed** |  |





***

### get_stored_auth_code



```php
protected get_stored_auth_code(mixed $code): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **mixed** |  |





***

### store_auth_code



```php
protected store_auth_code(mixed $code, mixed $client_id, mixed $redirect_uri, mixed $expires, mixed $scope): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **mixed** |  |
| `$client_id` | **mixed** |  |
| `$redirect_uri` | **mixed** |  |
| `$expires` | **mixed** |  |
| `$scope` | **mixed** |  |





***

### check_user_credentials



```php
protected check_user_credentials(mixed $client_id, mixed $username, mixed $password): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$username` | **mixed** |  |
| `$password` | **mixed** |  |





***

### check_assertion



```php
protected check_assertion(mixed $client_id, mixed $assertion_type, mixed $assertion): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$assertion_type` | **mixed** |  |
| `$assertion` | **mixed** |  |





***

### get_refresh_token



```php
protected get_refresh_token(mixed $refresh_token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$refresh_token` | **mixed** |  |





***

### store_refresh_token



```php
protected store_refresh_token(mixed $token, mixed $client_id, mixed $expires, mixed $scope = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |
| `$client_id` | **mixed** |  |
| `$expires` | **mixed** |  |
| `$scope` | **mixed** |  |





***

### check_none_access



```php
protected check_none_access(mixed $client_id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |





***

### get_default_authentication_realm



```php
protected get_default_authentication_realm(): mixed
```












***

### __construct



```php
public __construct(mixed $access_token_lifetime = 3600, mixed $auth_code_lifetime = 30, mixed $refresh_token_lifetime = 1209600): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$access_token_lifetime` | **mixed** |  |
| `$auth_code_lifetime` | **mixed** |  |
| `$refresh_token_lifetime` | **mixed** |  |





***

### verify_access_token



```php
public verify_access_token(mixed $scope = null, mixed $exit_not_present = true, mixed $exit_invalid = true, mixed $exit_expired = true, mixed $exit_scope = true, mixed $realm = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scope` | **mixed** |  |
| `$exit_not_present` | **mixed** |  |
| `$exit_invalid` | **mixed** |  |
| `$exit_expired` | **mixed** |  |
| `$exit_scope` | **mixed** |  |
| `$realm` | **mixed** |  |





***

### check_scope



```php
private check_scope(mixed $required_scope, mixed $available_scope): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$required_scope` | **mixed** |  |
| `$available_scope` | **mixed** |  |





***

### send_401_unauthorized



```php
private send_401_unauthorized(mixed $realm, mixed $scope, mixed $error = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$realm` | **mixed** |  |
| `$scope` | **mixed** |  |
| `$error` | **mixed** |  |





***

### get_access_token_param



```php
private get_access_token_param(): mixed
```












***

### grant_access_token



```php
public grant_access_token(): mixed
```












***

### get_client_credentials



```php
private get_client_credentials(): mixed
```












***

### get_authorize_params



```php
public get_authorize_params(): mixed
```












***

### finish_client_authorization



```php
public finish_client_authorization(mixed $is_authorized, mixed $type, mixed $client_id, mixed $redirect_uri, mixed $state, mixed $scope = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$is_authorized` | **mixed** |  |
| `$type` | **mixed** |  |
| `$client_id` | **mixed** |  |
| `$redirect_uri` | **mixed** |  |
| `$state` | **mixed** |  |
| `$scope` | **mixed** |  |





***

### do_redirect_uri_callback



```php
private do_redirect_uri_callback(mixed $redirect_uri, mixed $result): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$redirect_uri` | **mixed** |  |
| `$result` | **mixed** |  |





***

### build_uri



```php
private build_uri(mixed $uri, mixed $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **mixed** |  |
| `$data` | **mixed** |  |





***

### create_access_token



```php
private create_access_token(mixed $client_id, mixed $scope): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$scope` | **mixed** |  |





***

### create_auth_code



```php
private create_auth_code(mixed $client_id, mixed $redirect_uri, mixed $scope): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$client_id` | **mixed** |  |
| `$redirect_uri` | **mixed** |  |
| `$scope` | **mixed** |  |





***

### gen_access_token



```php
private gen_access_token(): mixed
```












***

### gen_auth_code



```php
private gen_auth_code(): mixed
```












***

### get_authorization_header



```php
private get_authorization_header(): mixed
```












***

### send_json_headers



```php
private send_json_headers(): mixed
```












***

### error



```php
public error(mixed $code, mixed $message = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **mixed** |  |
| `$message` | **mixed** |  |





***

### callback_error



```php
public callback_error(mixed $redirect_uri, mixed $error, mixed $state, mixed $message = null, mixed $error_uri = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$redirect_uri` | **mixed** |  |
| `$error` | **mixed** |  |
| `$state` | **mixed** |  |
| `$message` | **mixed** |  |
| `$error_uri` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
