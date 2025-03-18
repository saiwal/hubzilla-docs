
# Factory

This class is used to load OTP object from a provisioning Uri.



* Full name: `\OTPHP\Factory`
* This class is marked as **final** and can't be subclassed
* This class implements:
[`\OTPHP\FactoryInterface`](./FactoryInterface.md)
* This class is a **Final class**

**See Also:**

* \OTPHP\Test\FactoryTest - 




## Methods


### loadFromProvisioningUri

This method is the unique public method of the class. It can load a provisioning Uri and convert it into an OTP
object.

```php
public static loadFromProvisioningUri(string $uri): \OTPHP\OTPInterface
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |





***

### populateParameters



```php
private static populateParameters(\OTPHP\OTPInterface $otp, \OTPHP\Url $data): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$otp` | **\OTPHP\OTPInterface** |  |
| `$data` | **\OTPHP\Url** |  |





***

### populateOTP



```php
private static populateOTP(\OTPHP\OTPInterface $otp, \OTPHP\Url $data): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$otp` | **\OTPHP\OTPInterface** |  |
| `$data` | **\OTPHP\Url** |  |





***

### createOTP



```php
private static createOTP(\OTPHP\Url $parsed_url): \OTPHP\OTPInterface
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parsed_url` | **\OTPHP\Url** |  |





***

### getLabel



```php
private static getLabel(non-empty-string $data): non-empty-string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **non-empty-string** |  |





***


***
> Automatically generated on 2025-03-18
