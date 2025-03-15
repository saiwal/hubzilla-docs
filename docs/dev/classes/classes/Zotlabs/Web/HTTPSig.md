***

# HTTPSig





* Full name: `\Zotlabs\Web\HTTPSig`

**See Also:**

* https://tools.ietf.org/html/draft-cavage-http-signatures-10 - 




## Methods


### generate_digest_header



```php
public static generate_digest_header(string $body, string $alg = &#039;sha256&#039;): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$body` | **string** | The value to create the digest for |
| `$alg` | **string** | hash algorithm (one of &#039;sha256&#039;,&#039;sha512&#039;) |


**Return Value:**

The generated digest header string for $body




**See Also:**

* https://tools.ietf.org/html/rfc5843 - 

***

### find_headers



```php
public static find_headers(mixed $data, mixed& $body): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$body` | **mixed** |  |





***

### verify



```php
public static verify(mixed $data, mixed $key = &#039;&#039;, mixed $keytype = &#039;&#039;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$key` | **mixed** |  |
| `$keytype` | **mixed** |  |





***

### get_key



```php
public static get_key(mixed $key, mixed $keytype, mixed $id, mixed $force = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** |  |
| `$keytype` | **mixed** |  |
| `$id` | **mixed** |  |
| `$force` | **mixed** |  |





***

### convertKey



```php
public static convertKey(mixed $key): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** |  |





***

### get_activitystreams_key



```php
public static get_activitystreams_key(string $id, bool $force = false, mixed $delete = false): bool|array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** |  |
| `$force` | **bool** | (optional, default false) |
| `$delete` | **mixed** |  |


**Return Value:**


false if no pub key found, otherwise return an array with the pub key




***

### get_webfinger_key



```php
public static get_webfinger_key(string $id, bool $force = false): bool|array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** |  |
| `$force` | **bool** | (optional, default false) |


**Return Value:**


false if no pub key found, otherwise return an array with the pub key




***

### get_zotfinger_key



```php
public static get_zotfinger_key(string $id, bool $force = false): bool|array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** |  |
| `$force` | **bool** | (optional, default false) |


**Return Value:**


false if no pub key found, otherwise return an array with the public key




***

### create_sig



```php
public static create_sig(array $head, string $prvkey, string $keyid = EMPTY_STR, bool $auth = false, string $alg = &#039;sha256&#039;, array $encryption = false): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$head` | **array** |  |
| `$prvkey` | **string** |  |
| `$keyid` | **string** | (optional, default &#039;&#039;) |
| `$auth` | **bool** | (optional, default false) |
| `$alg` | **string** | (optional, default &#039;sha256&#039;) |
| `$encryption` | **array** | [ &#039;key&#039;, &#039;algorithm&#039; ] or false |





***

### set_headers



```php
public static set_headers(array $headers): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$headers` | **array** |  |





***

### sign



```php
public static sign(array $head, string $prvkey, string $alg = &#039;sha256&#039;): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$head` | **array** |  |
| `$prvkey` | **string** |  |
| `$alg` | **string** | (optional) default &#039;sha256&#039; |





***

### parse_sigheader



```php
public static parse_sigheader(string $header): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$header` | **string** |  |


**Return Value:**

associate array with
- \e string \b keyID
- \e string \b algorithm
- \e array  \b headers
- \e string \b signature




***

### decrypt_sigheader



```php
public static decrypt_sigheader(string $header, string $prvkey = null): array|string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$header` | **string** |  |
| `$prvkey` | **string** | (optional), if not set use site private key |


**Return Value:**

associative array, empty string if failue
- \e string \b iv
- \e string \b key
- \e string \b alg
- \e string \b data




***


***
> Automatically generated on 2025-03-15
