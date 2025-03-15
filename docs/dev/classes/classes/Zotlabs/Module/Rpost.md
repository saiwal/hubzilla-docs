***

# Rpost

remote post

https://yoursite/rpost?f=&title=&body=&remote_return=

This can be called via either GET or POST, use POST for long body content as suhosin often limits GET parameter length

f= placeholder, often required
title= Title of post
body= Body of post
url= URL which will be parsed and the results appended to the body
source= Source application
post_id= post_id of post to 'share' (local use only)
remote_return= absolute URL to return after posting is finished
type= choices are 'html' or 'bbcode', default is 'bbcode'

* Full name: `\Zotlabs\Module\Rpost`
* Parent class: [`\Zotlabs\Web\Controller`](../Web/Controller.md)




## Methods


### get

Handle requests.

```php
public get(): string
```

Despite it's name, this method handles both POST and GET requests
to the module.







**Return Value:**

HTML content for the module.




***

### redirect_or_login

Redirect to the observer's instance if not local, or return login form.

```php
private redirect_or_login(): string
```

The request is saved in the session if there's a `body` request
param present. (Otherwise not.)







**Return Value:**

A login form if not redirected. If the session was
determned to belong to a remote channel, the function does not
return.




***

### handle_attachments

Handle uplads of attachments in the rpost call.

```php
private handle_attachments(): void
```

This is only relevant for POST requests.

The function will modify the `$_REQUEST['body']` superglobal
(or add it if it does not exist).










***


## Inherited methods


### init

Initialize request processing.

```php
public init(): mixed
```

This method is called before any other request processing, and
regardless of the request method. The theme is not yet loaded when
this method is invoked.










***

### post

Process POST requests.

```php
public post(): mixed
```

This method is called if the incoming request is a POST request. It is
invoked after the theme has been loaded. This method should not normally
render HTML output, as processing will fall through to the GET processing
if this method completes without error or stopping processing in other
ways.










***

### get

Process GET requests or the body part of POST requests.

```php
public get(): string
```

This method is called directly for GET requests, and immediately after the
`post()` method for POST requests.

It will return the module content as a HTML string.







**Return Value:**

HTML content for the module.




***


***
> Automatically generated on 2025-03-15
