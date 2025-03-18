
# MysqlProvider

Using this class, you can easily set up an OpenID Provider.

It's independent of LightOpenID class.
It requires either GMP or BCMath for session encryption,
but will work without them (although either via SSL, or in stateless mode only).
Also, it requires PHP >= 5.1.2

This is an alpha version, using it in production code is not recommended,
until you are *sure* that it works and is secure.

Please send me messages about your testing results
(even if successful, so I know that it has been tested).
Also, if you think there's a way to make it easier to use, tell me -- it's an alpha for a reason.
Same thing applies to bugs in code, suggestions,
and everything else you'd like to say about the library.

There's no usage documentation here, see the examples.

* Full name: `\MysqlProvider`
* Parent class: [`\LightOpenIDProvider`](./LightOpenIDProvider.md)



## Properties


### attrMap



```php
private $attrMap
```






***

### attrFieldMap



```php
private $attrFieldMap
```






***

## Methods


### setup

Displays an user interface for inputting user's login and password.

```php
public setup(mixed $identity, mixed $realm, mixed $assoc_handle, mixed $attributes): mixed
```

Attributes are always AX field namespaces, with stripped host part.
For example, the $attributes array may be:
array( 'required' => array('namePerson/friendly', 'contact/email'),
       'optional' => array('pref/timezone', 'pref/language')






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$identity` | **mixed** | Discovered identity string. May be used to extract login, unless using $this-&gt;select_id |
| `$realm` | **mixed** | Realm used for authentication. |
| `$assoc_handle` | **mixed** |  |
| `$attributes` | **mixed** |  |





***

### checkid

Checks whether an user is authenticated.

```php
public checkid(mixed $realm, mixed& $attributes): string
```

The function should determine what fields it wants to send to the RP,
and put them in the $attributes array.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$realm` | **mixed** | Realm used for authentication. |
| `$attributes` | **mixed** |  |


**Return Value:**

OP-local identifier of an authenticated user, or an empty value.




***

### assoc_handle

Generates a new association handle.

```php
public assoc_handle(): string
```












***

### setAssoc

Stores an association.

```php
public setAssoc(mixed $handle, mixed $data): mixed
```

If you want to use php sessions in your provider code, you have to replace it.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$handle` | **mixed** | Association handle -- should be used as a key. |
| `$data` | **mixed** |  |





***

### getAssoc

Retreives association data.

```php
public getAssoc(mixed $handle): array
```

If you want to use php sessions in your provider code, you have to replace it.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$handle` | **mixed** | Association handle. |


**Return Value:**

Association data.




***

### delAssoc

Deletes an association.

```php
public delAssoc(mixed $handle): mixed
```

If you want to use php sessions in your provider code, you have to replace it.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$handle` | **mixed** | Association handle. |





***


## Inherited methods


### checkid

Checks whether an user is authenticated.

```php
public checkid(string $realm, array& $attributes): string
```

The function should determine what fields it wants to send to the RP,
and put them in the $attributes array.


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$realm` | **string** | Realm used for authentication. |
| `$attributes` | **array** |  |


**Return Value:**

OP-local identifier of an authenticated user, or an empty value.




***

### setup

Displays an user interface for inputting user's login and password.

```php
public setup(string $identity, string $realm, mixed $assoc_handle, mixed $attributes): mixed
```

Attributes are always AX field namespaces, with stripped host part.
For example, the $attributes array may be:
array( 'required' => array('namePerson/friendly', 'contact/email'),
       'optional' => array('pref/timezone', 'pref/language')


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$identity` | **string** | Discovered identity string. May be used to extract login, unless using $this-&gt;select_id |
| `$realm` | **string** | Realm used for authentication. |
| `$assoc_handle` | **mixed** |  |
| `$attributes` | **mixed** |  |





***

### setAssoc

Stores an association.

```php
protected setAssoc(string $handle, array $assoc): mixed
```

If you want to use php sessions in your provider code, you have to replace it.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$handle` | **string** | Association handle -- should be used as a key. |
| `$assoc` | **array** | Association data. |





***

### getAssoc

Retreives association data.

```php
protected getAssoc(string $handle): array
```

If you want to use php sessions in your provider code, you have to replace it.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$handle` | **string** | Association handle. |


**Return Value:**

Association data.




***

### delAssoc

Deletes an association.

```php
protected delAssoc(string $handle): mixed
```

If you want to use php sessions in your provider code, you have to replace it.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$handle` | **string** | Association handle. |





***

### redirect

Redirects the user to an url.

```php
protected redirect(string $location): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$location` | **string** | The url that the user will be redirected to. |





***

### assoc_handle

Generates a new association handle.

```php
protected assoc_handle(): string
```












***

### shared_secret

Generates a random shared secret.

```php
protected shared_secret(mixed $hash): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hash` | **mixed** |  |





***

### keygen

Generates a private key.

```php
protected keygen(int $length): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$length` | **int** | Length of the key. |





***

### __construct



```php
public __construct(): mixed
```












***

### xrds

Displays an XRDS document, or redirects to it.

```php
public xrds(bool|null $force = null): mixed
```

By default, it detects whether it should display or redirect automatically.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$force` | **bool&#124;null** | When true, always display the document, when false always redirect. |





***

### xrdsContent

Returns the content of the XRDS document

```php
protected xrdsContent(): string
```









**Return Value:**

The XRDS document.




***

### server

Does everything that a provider has to -- in one function.

```php
public server(): mixed
```












***

### checkRealm



```php
protected checkRealm(): mixed
```












***

### ax



```php
protected ax(): mixed
```












***

### sreg



```php
protected sreg(): mixed
```












***

### verify

Aids an RP in assertion verification.

```php
protected verify(): bool
```









**Return Value:**

Information whether the verification suceeded.




***

### associate

Performs association with an RP.

```php
protected associate(): mixed
```












***

### generateAssociation

Creates a private association.

```php
protected generateAssociation(): mixed
```












***

### dh

Encrypts the MAC key using DH key exchange.

```php
protected dh(): mixed
```












***

### x_or

XORs two strings.

```php
protected x_or(string $a, string $b): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$a` | **string** |  |
| `$b` | **string** |  |


**Return Value:**

$a ^ $b




***

### response

Prepares an indirect response url.

```php
protected response(array $params): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$params` | **array** | Parameters to be sent. |





***

### errorResponse

Outputs a direct error.

```php
protected errorResponse(): mixed
```












***

### positiveResponse

Sends an positive assertion.

```php
protected positiveResponse(string $identity, array $attributes): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$identity` | **string** | the OP-Local Identifier that is being authenticated. |
| `$attributes` | **array** | User attributes to be sent. |





***

### responseAttributes

Prepares an array of attributes to send

```php
protected responseAttributes(mixed $attributes): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attributes` | **mixed** |  |





***

### keyValueForm

Encodes fields in key-value form.

```php
protected keyValueForm(array $params): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$params` | **array** | Fields to be encoded. |


**Return Value:**

$params in key-value form.




***

### cancel

Responds with an information that the user has canceled authentication.

```php
protected cancel(): mixed
```












***

### b64dec

Converts base64 encoded number to it's decimal representation.

```php
protected b64dec(string $str): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** | base64 encoded number. |


**Return Value:**

Decimal representation of that number.




***

### decb64

Complements b64dec.

```php
protected decb64(mixed $num): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$num` | **mixed** |  |





***

### __call



```php
public __call(mixed $name, mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |
| `$args` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
