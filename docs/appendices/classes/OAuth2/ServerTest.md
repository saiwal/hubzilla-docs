
# ServerTest





* Full name: `\OAuth2\ServerTest`
* Parent class: [`TestCase`](../PHPUnit/Framework/TestCase.md)




## Methods


### testGetAuthorizeControllerWithNoClientStorageThrowsException



```php
public testGetAuthorizeControllerWithNoClientStorageThrowsException(): mixed
```












***

### testGetAuthorizeControllerWithNoAccessTokenStorageThrowsException



```php
public testGetAuthorizeControllerWithNoAccessTokenStorageThrowsException(): mixed
```












***

### testGetAuthorizeControllerWithClientStorageAndAccessTokenResponseType



```php
public testGetAuthorizeControllerWithClientStorageAndAccessTokenResponseType(): mixed
```












***

### testGetAuthorizeControllerWithClientStorageAndAuthorizationCodeResponseType



```php
public testGetAuthorizeControllerWithClientStorageAndAuthorizationCodeResponseType(): mixed
```












***

### testGetAuthorizeControllerWithClientStorageAndAccessTokenStorageThrowsException



```php
public testGetAuthorizeControllerWithClientStorageAndAccessTokenStorageThrowsException(): mixed
```












***

### testGetAuthorizeControllerWithClientStorageAndAccessTokenStorage



```php
public testGetAuthorizeControllerWithClientStorageAndAccessTokenStorage(): mixed
```












***

### testGetAuthorizeControllerWithClientStorageAndAuthorizationCodeStorage



```php
public testGetAuthorizeControllerWithClientStorageAndAuthorizationCodeStorage(): mixed
```












***

### testGetTokenControllerWithGrantTypeStorageThrowsException



```php
public testGetTokenControllerWithGrantTypeStorageThrowsException(): mixed
```












***

### testGetTokenControllerWithNoClientCredentialsStorageThrowsException



```php
public testGetTokenControllerWithNoClientCredentialsStorageThrowsException(): mixed
```












***

### testGetTokenControllerWithNoAccessTokenStorageThrowsException



```php
public testGetTokenControllerWithNoAccessTokenStorageThrowsException(): mixed
```












***

### testGetTokenControllerWithAccessTokenAndClientCredentialsStorage



```php
public testGetTokenControllerWithAccessTokenAndClientCredentialsStorage(): mixed
```












***

### testGetTokenControllerAccessTokenStorageAndClientCredentialsStorageAndGrantTypes



```php
public testGetTokenControllerAccessTokenStorageAndClientCredentialsStorageAndGrantTypes(): mixed
```












***

### testGetResourceControllerWithNoAccessTokenStorageThrowsException



```php
public testGetResourceControllerWithNoAccessTokenStorageThrowsException(): mixed
```












***

### testGetResourceControllerWithAccessTokenStorage



```php
public testGetResourceControllerWithAccessTokenStorage(): mixed
```












***

### testAddingStorageWithInvalidClass



```php
public testAddingStorageWithInvalidClass(): mixed
```












***

### testAddingStorageWithInvalidKey



```php
public testAddingStorageWithInvalidKey(): mixed
```












***

### testAddingStorageWithInvalidKeyStorageCombination



```php
public testAddingStorageWithInvalidKeyStorageCombination(): mixed
```












***

### testAddingStorageWithValidKeyOnlySetsThatKey



```php
public testAddingStorageWithValidKeyOnlySetsThatKey(): mixed
```












***

### testAddingClientStorageSetsClientCredentialsStorageByDefault



```php
public testAddingClientStorageSetsClientCredentialsStorageByDefault(): mixed
```












***

### testAddStorageWithNullValue



```php
public testAddStorageWithNullValue(): mixed
```












***

### testNewServerWithNullStorageValue



```php
public testNewServerWithNullStorageValue(): mixed
```












***

### testAddingClientCredentialsStorageSetsClientStorageByDefault



```php
public testAddingClientCredentialsStorageSetsClientStorageByDefault(): mixed
```












***

### testSettingClientStorageByDefaultDoesNotOverrideSetStorage



```php
public testSettingClientStorageByDefaultDoesNotOverrideSetStorage(): mixed
```












***

### testAddingResponseType



```php
public testAddingResponseType(): mixed
```












***

### testCustomClientAssertionType



```php
public testCustomClientAssertionType(): mixed
```












***

### testHttpBasicConfig



```php
public testHttpBasicConfig(): mixed
```












***

### testRefreshTokenConfig



```php
public testRefreshTokenConfig(): mixed
```












***

### testValidRefreshTokenWithNewRefreshTokenInResponse

Test setting "always_issue_new_refresh_token" on a server level

```php
public testValidRefreshTokenWithNewRefreshTokenInResponse(): mixed
```












**See Also:**

*  - test/OAuth2/GrantType/RefreshTokenTest::testValidRefreshTokenWithNewRefreshTokenInResponse

***

### testAddingUnknownResponseTypeThrowsException



```php
public testAddingUnknownResponseTypeThrowsException(): mixed
```












***

### testUsingJwtAccessTokensWithoutPublicKeyStorageThrowsException



```php
public testUsingJwtAccessTokensWithoutPublicKeyStorageThrowsException(): mixed
```












***

### testUsingJustJwtAccessTokenStorageWithResourceControllerIsOkay



```php
public testUsingJustJwtAccessTokenStorageWithResourceControllerIsOkay(): mixed
```












***

### testUsingJustJwtAccessTokenStorageWithAuthorizeControllerThrowsException



```php
public testUsingJustJwtAccessTokenStorageWithAuthorizeControllerThrowsException(): mixed
```












***

### testUsingJustJwtAccessTokenStorageWithTokenControllerThrowsException



```php
public testUsingJustJwtAccessTokenStorageWithTokenControllerThrowsException(): mixed
```












***

### testUsingJwtAccessTokenAndClientStorageWithAuthorizeControllerIsOkay



```php
public testUsingJwtAccessTokenAndClientStorageWithAuthorizeControllerIsOkay(): mixed
```












***

### testUsingOpenIDConnectWithoutUserClaimsThrowsException



```php
public testUsingOpenIDConnectWithoutUserClaimsThrowsException(): mixed
```












***

### testUsingOpenIDConnectWithoutPublicKeyThrowsException



```php
public testUsingOpenIDConnectWithoutPublicKeyThrowsException(): mixed
```












***

### testUsingOpenIDConnectWithoutIssuerThrowsException



```php
public testUsingOpenIDConnectWithoutIssuerThrowsException(): mixed
```












***

### testUsingOpenIDConnectWithIssuerPublicKeyAndUserClaimsIsOkay



```php
public testUsingOpenIDConnectWithIssuerPublicKeyAndUserClaimsIsOkay(): mixed
```












***

### testUsingOpenIDConnectWithAllowImplicitWithoutTokenStorageThrowsException



```php
public testUsingOpenIDConnectWithAllowImplicitWithoutTokenStorageThrowsException(): mixed
```












***

### testUsingOpenIDConnectWithAllowImplicitAndUseJwtAccessTokensIsOkay



```php
public testUsingOpenIDConnectWithAllowImplicitAndUseJwtAccessTokensIsOkay(): mixed
```












***

### testUsingOpenIDConnectWithAllowImplicitAndAccessTokenStorageIsOkay



```php
public testUsingOpenIDConnectWithAllowImplicitAndAccessTokenStorageIsOkay(): mixed
```












***

### testUsingOpenIDConnectWithAllowImplicitAndAccessTokenResponseTypeIsOkay



```php
public testUsingOpenIDConnectWithAllowImplicitAndAccessTokenResponseTypeIsOkay(): mixed
```












***

### testUsingOpenIDConnectWithAuthorizationCodeStorageThrowsException



```php
public testUsingOpenIDConnectWithAuthorizationCodeStorageThrowsException(): mixed
```












***

### testUsingOpenIDConnectWithOpenIDAuthorizationCodeStorageCreatesOpenIDAuthorizationCodeGrantType



```php
public testUsingOpenIDConnectWithOpenIDAuthorizationCodeStorageCreatesOpenIDAuthorizationCodeGrantType(): mixed
```












***

### testMultipleValuedResponseTypeOrderDoesntMatter



```php
public testMultipleValuedResponseTypeOrderDoesntMatter(): mixed
```












***

### testAddGrantTypeWithoutKey



```php
public testAddGrantTypeWithoutKey(): mixed
```












***

### testAddGrantTypeWithKey



```php
public testAddGrantTypeWithKey(): mixed
```












***

### testAddGrantTypeWithKeyNotString



```php
public testAddGrantTypeWithKeyNotString(): mixed
```












***


***
> Automatically generated on 2025-03-18
