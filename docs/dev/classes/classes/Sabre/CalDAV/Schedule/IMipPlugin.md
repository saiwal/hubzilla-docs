
# IMipPlugin

iMIP handler.

This class is responsible for sending out iMIP messages. iMIP is the
email-based transport for iTIP. iTIP deals with scheduling operations for
iCalendar objects.

If you want to customize the email that gets sent out, you can do so by
extending this class and overriding the sendMessage method.

* Full name: `\Sabre\CalDAV\Schedule\IMipPlugin`
* Parent class: [`\Sabre\DAV\ServerPlugin`](../../DAV/ServerPlugin.md)



## Properties


### senderEmail

Email address used in From: header.

```php
protected string $senderEmail
```






***

## Methods


### __construct

Creates the email handler.

```php
public __construct(string $senderEmail): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$senderEmail` | **string** | . The &#039;senderEmail&#039; is the email that shows up<br />in the &#039;From:&#039; address. This should<br />generally be some kind of no-reply email<br />address you own. |





***

### initialize

This initializes the plugin.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```

This function is called by Sabre\DAV\Server, after
addPlugin is called.

This method should set up the required event subscriptions.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





***

### getPluginName

Returns a plugin name.

```php
public getPluginName(): string
```

Using this name other plugins will be able to access other plugins
using \Sabre\DAV\Server::getPlugin










***

### schedule

Event handler for the 'schedule' event.

```php
public schedule(\Sabre\VObject\ITip\Message $iTipMessage): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$iTipMessage` | **\Sabre\VObject\ITip\Message** |  |





***

### mail

This function is responsible for sending the actual email.

```php
protected mail(string $to, string $subject, string $body, array $headers): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$to` | **string** | Recipient email address |
| `$subject` | **string** | Subject of the email |
| `$body` | **string** | iCalendar body |
| `$headers` | **array** | List of headers |





***

### getPluginInfo

Returns a bunch of meta-data about the plugin.

```php
public getPluginInfo(): array
```

Providing this information is optional, and is mainly displayed by the
Browser plugin.

The description key in the returned array may contain html and will not
be sanitized.










***


## Inherited methods


### initialize

This initializes the plugin.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```

This function is called by Sabre\DAV\Server, after
addPlugin is called.

This method should set up the required event subscriptions.


* This method is **abstract**.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





***

### getFeatures

This method should return a list of server-features.

```php
public getFeatures(): array
```

This is for example 'versioning' and is added to the DAV: header
in an OPTIONS response.










***

### getHTTPMethods

Use this method to tell the server this plugin defines additional
HTTP methods.

```php
public getHTTPMethods(string $path): array
```

This method is passed a uri. It should only return HTTP methods that are
available for the specified uri.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### getPluginName

Returns a plugin name.

```php
public getPluginName(): string
```

Using this name other plugins will be able to access other plugins
using \Sabre\DAV\Server::getPlugin










***

### getSupportedReportSet

Returns a list of reports this plugin supports.

```php
public getSupportedReportSet(string $uri): array
```

This will be used in the {DAV:}supported-report-set property.
Note that you still need to subscribe to the 'report' event to actually
implement them






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |





***

### getPluginInfo

Returns a bunch of meta-data about the plugin.

```php
public getPluginInfo(): array
```

Providing this information is optional, and is mainly displayed by the
Browser plugin.

The description key in the returned array may contain html and will not
be sanitized.










***


***
> Automatically generated on 2025-03-15
