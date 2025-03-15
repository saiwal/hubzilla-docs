
# INode

This node represents a single notification.

The signature is mostly identical to that of Sabre\DAV\IFile, but the get() method
MUST return an xml document that matches the requirements of the
'caldav-notifications.txt' spec.

For a complete example, check out the Notification class, which contains
some helper functions.

* Full name: `\Sabre\CalDAV\Notifications\INode`



## Methods


### getNotificationType

This method must return an xml element, using the
Sabre\CalDAV\Xml\Notification\NotificationInterface classes.

```php
public getNotificationType(): \Sabre\CalDAV\Xml\Notification\NotificationInterface
```












***

### getETag

Returns the etag for the notification.

```php
public getETag(): string
```

The etag must be surrounded by literal double-quotes.










***


***
> Automatically generated on 2025-03-15
