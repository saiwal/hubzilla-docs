
# Sapi

PHP SAPI.

This object is responsible for:
1. Constructing a Request object based on the current HTTP request sent to
   the PHP process.
2. Sending the Response object back to the client.

It could be said that this class provides a mapping between the Request and
Response objects, and php's:

* $_SERVER
* $_POST
* $_FILES
* php://input
* echo()
* header()
* php://output

You can choose to either call all these methods statically, but you can also
instantiate this as an object to allow for polymorphism.

* Full name: `\Sabre\HTTP\Sapi`




## Methods


### getRequest

This static method will create a new Request object, based on the
current PHP request.

```php
public static getRequest(): \Sabre\HTTP\Request
```



* This method is **static**.








***

### sendResponse

Sends the HTTP response back to a HTTP client.

```php
public static sendResponse(\Sabre\HTTP\ResponseInterface $response): mixed
```

This calls php's header() function and streams the body to php://output.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### createFromServerArray

This static method will create a new Request object, based on a PHP
$_SERVER array.

```php
public static createFromServerArray(array $serverArray): \Sabre\HTTP\Request
```

REQUEST_URI and REQUEST_METHOD are required.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$serverArray` | **array** |  |





***


***
> Automatically generated on 2025-03-15
