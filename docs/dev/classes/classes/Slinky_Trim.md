***

# Slinky_Trim

Use this class to create a Service implementation for your own URL
shortening service. Extend the class and customize methods to suit your
service. Note that it is an "abstract" class, so there are certain methods
which you *must* define.



* Full name: `\Slinky_Trim`
* Parent class: [`\Slinky_Service`](./Slinky_Service.md)




## Methods


### url_is_short

Determine, based on the input URL, if it's already a short URL, from
this particular service. e.g. a Bit.ly URL contains "bit.ly/"

```php
public url_is_short(mixed $url): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### url_is_long

Determine if this is a "long" URL (just means it hasn't been shortened)
already. e.g. a no-Bit.ly URL would NOT contain "bit.ly/"

```php
public url_is_long(mixed $url): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### make_short

Handle taking the $url and converting it to a short URL via whatever
means is provided at the remote service.

```php
public make_short(mixed $url): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### make_long

Return the long/expanded version of a URL via any API means available
from this service. As a fallback, you might
consider just following the URL and using SLINKY_FINAL_URL as the
return method from a $this->url_get() call to find out.

```php
public make_long(mixed $url): mixed
```

This one is optional for Services extending this class, if they don't
then the following implementation will work on most services anyway.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***


## Inherited methods


### url_is_short

Determine, based on the input URL, if it's already a short URL, from
this particular service. e.g. a Bit.ly URL contains "bit.ly/"

```php
public url_is_short(mixed $url): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### url_is_long

Determine if this is a "long" URL (just means it hasn't been shortened)
already. e.g. a no-Bit.ly URL would NOT contain "bit.ly/"

```php
public url_is_long(mixed $url): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### make_short

Handle taking the $url and converting it to a short URL via whatever
means is provided at the remote service.

```php
public make_short(mixed $url): mixed
```




* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### make_long

Return the long/expanded version of a URL via any API means available
from this service. As a fallback, you might
consider just following the URL and using SLINKY_FINAL_URL as the
return method from a $this->url_get() call to find out.

```php
public make_long(mixed $url): mixed
```

This one is optional for Services extending this class, if they don't
then the following implementation will work on most services anyway.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### get

Method for getting properties that you might need during the process
of shortening/lengthening a URL (e.g. auth credentials)

```php
public get(mixed $prop): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prop` | **mixed** |  |





***

### set

Method for setting properties that you might need during the process
of shortening/lengthening a URL (e.g. auth credentials)

```php
public set(mixed $prop, mixed $val): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prop` | **mixed** |  |
| `$val` | **mixed** |  |





***

### url_get

Internal helper for performing a GET request on a remote URL.

```php
protected url_get(string $url, \const $return = SLINKY_BODY): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** | The URL to GET |
| `$return` | **\const** | The return method [ SLINKY_BODY &amp;#124; SLINKY_FINAL_URL &amp;#124; SLINKY_HEADERS ] |





***

### url_post

Internal helper for performing a POST request on a remote URL.

```php
protected url_post(string $url, array $payload = array(), \const $return = SLINKY_BODY): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** | The URL to POST to |
| `$payload` | **array** | Array containing name/value pairs of the parameters to POST |
| `$return` | **\const** | The return method [ SLINKY_BODY &amp;#124; SLINKY_FINAL_URL &amp;#124; SLINKY_HEADERS ] |





***


***
> Automatically generated on 2025-03-15
