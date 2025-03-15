
# JwtBearerTest





* Full name: `\OAuth2\GrantType\JwtBearerTest`
* Parent class: [`TestCase`](../../PHPUnit/Framework/TestCase.md)



## Properties


### privateKey



```php
private $privateKey
```






***

## Methods


### setUp



```php
public setUp(): void
```












***

### testMalformedJWT



```php
public testMalformedJWT(): mixed
```












***

### testBrokenSignature



```php
public testBrokenSignature(): mixed
```












***

### testExpiredJWT



```php
public testExpiredJWT(): mixed
```












***

### testBadExp



```php
public testBadExp(): mixed
```












***

### testNoAssert



```php
public testNoAssert(): mixed
```












***

### testNotBefore



```php
public testNotBefore(): mixed
```












***

### testBadNotBefore



```php
public testBadNotBefore(): mixed
```












***

### testNonMatchingAudience



```php
public testNonMatchingAudience(): mixed
```












***

### testBadClientID



```php
public testBadClientID(): mixed
```












***

### testBadSubject



```php
public testBadSubject(): mixed
```












***

### testMissingKey



```php
public testMissingKey(): mixed
```












***

### testValidJwt



```php
public testValidJwt(): mixed
```












***

### testValidJwtWithScope



```php
public testValidJwtWithScope(): mixed
```












***

### testValidJwtInvalidScope



```php
public testValidJwtInvalidScope(): mixed
```












***

### testValidJti



```php
public testValidJti(): mixed
```












***

### testInvalidJti



```php
public testInvalidJti(): mixed
```












***

### testJtiReplayAttack



```php
public testJtiReplayAttack(): mixed
```












***

### getJWT

Generates a JWT

```php
private getJWT(mixed $exp = null, mixed $nbf = null, mixed $sub = null, mixed $iss = &#039;Test Client ID&#039;, mixed $jti = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$exp` | **mixed** | The expiration date. If the current time is greater than the exp, the JWT is invalid. |
| `$nbf` | **mixed** | The &quot;not before&quot; time. If the current time is less than the nbf, the JWT is invalid. |
| `$sub` | **mixed** | The subject we are acting on behalf of. This could be the email address of the user in the system. |
| `$iss` | **mixed** | The issuer, usually the client_id. |
| `$jti` | **mixed** |  |





***

### getTestServer



```php
private getTestServer(mixed $audience = &#039;http://myapp.com/oauth/auth&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$audience` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
