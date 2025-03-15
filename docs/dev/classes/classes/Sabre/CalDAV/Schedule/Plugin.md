***

# Plugin

CalDAV scheduling plugin.

=========================.

This plugin provides the functionality added by the "Scheduling Extensions
to CalDAV" standard, as defined in RFC6638.

calendar-auto-schedule largely works by intercepting a users request to
update their local calendar. If a user creates a new event with attendees,
this plugin is supposed to grab the information from that event, and notify
the attendees of this.

There's 3 possible transports for this:
* local delivery
* delivery through email (iMip)
* server-to-server delivery (iSchedule)

iMip is simply, because we just need to add the iTip message as an email
attachment. Local delivery is harder, because we both need to add this same
message to a local DAV inbox, as well as live-update the relevant events.

iSchedule is something for later.

* Full name: `\Sabre\CalDAV\Schedule\Plugin`
* Parent class: [`\Sabre\DAV\ServerPlugin`](../../DAV/ServerPlugin.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`NS_CALDAV`|public| |&#039;urn:ietf:params:xml:ns:caldav&#039;|

## Properties


### server

Reference to main Server object.

```php
protected \Sabre\DAV\Server $server
```






***

## Methods


### getFeatures

Returns a list of features for the DAV: HTTP header.

```php
public getFeatures(): array
```












***

### getPluginName

Returns the name of the plugin.

```php
public getPluginName(): string
```

Using this name other plugins will be able to access other plugins
using Server::getPlugin










***

### initialize

Initializes the plugin.

```php
public initialize(\Sabre\DAV\Server $server): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$server` | **\Sabre\DAV\Server** |  |





***

### getHTTPMethods

Use this method to tell the server this plugin defines additional
HTTP methods.

```php
public getHTTPMethods(string $uri): array
```

This method is passed a uri. It should only return HTTP methods that are
available for the specified uri.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uri` | **string** |  |





***

### httpPost

This method handles POST request for the outbox.

```php
public httpPost(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### propFind

This method handler is invoked during fetching of properties.

```php
public propFind(\Sabre\DAV\PropFind $propFind, \Sabre\DAV\INode $node): mixed
```

We use this event to add calendar-auto-schedule-specific properties.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propFind` | **\Sabre\DAV\PropFind** |  |
| `$node` | **\Sabre\DAV\INode** |  |





***

### propPatch

This method is called during property updates.

```php
public propPatch(string $path, \Sabre\DAV\PropPatch $propPatch): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$propPatch` | **\Sabre\DAV\PropPatch** |  |





***

### calendarObjectChange

This method is triggered whenever there was a calendar object gets
created or updated.

```php
public calendarObjectChange(\Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response, \Sabre\VObject\Component\VCalendar $vCal, mixed $calendarPath, mixed& $modified, mixed $isNew): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** | HTTP request |
| `$response` | **\Sabre\HTTP\ResponseInterface** | HTTP Response |
| `$vCal` | **\Sabre\VObject\Component\VCalendar** | Parsed iCalendar object |
| `$calendarPath` | **mixed** | Path to calendar collection |
| `$modified` | **mixed** | the iCalendar object has been touched |
| `$isNew` | **mixed** | Whether this was a new item or we&#039;re updating one |





***

### deliver

This method is responsible for delivering the ITip message.

```php
public deliver(\Sabre\VObject\ITip\Message $iTipMessage): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$iTipMessage` | **\Sabre\VObject\ITip\Message** |  |





***

### beforeUnbind

This method is triggered before a file gets deleted.

```php
public beforeUnbind(string $path): mixed
```

We use this event to make sure that when this happens, attendees get
cancellations, and organizers get 'DECLINED' statuses.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### scheduleLocalDelivery

Event handler for the 'schedule' event.

```php
public scheduleLocalDelivery(\Sabre\VObject\ITip\Message $iTipMessage): mixed
```

This handler attempts to look at local accounts to deliver the
scheduling object.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$iTipMessage` | **\Sabre\VObject\ITip\Message** |  |





***

### getSupportedPrivilegeSet

This method is triggered whenever a subsystem requests the privileges
that are supported on a particular node.

```php
public getSupportedPrivilegeSet(\Sabre\DAV\INode $node, array& $supportedPrivilegeSet): mixed
```

We need to add a number of privileges for scheduling purposes.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\Sabre\DAV\INode** |  |
| `$supportedPrivilegeSet` | **array** |  |





***

### processICalendarChange

This method looks at an old iCalendar object, a new iCalendar object and
starts sending scheduling messages based on the changes.

```php
protected processICalendarChange(\Sabre\VObject\Component\VCalendar|string|null $oldObject, \Sabre\VObject\Component\VCalendar $newObject, array $addresses, array $ignore = [], bool& $modified = false): mixed
```

A list of addresses needs to be specified, so the system knows who made
the update, because the behavior may be different based on if it's an
attendee or an organizer.

This method may update $newObject to add any status changes.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$oldObject` | **\Sabre\VObject\Component\VCalendar&#124;string&#124;null** |  |
| `$newObject` | **\Sabre\VObject\Component\VCalendar** |  |
| `$addresses` | **array** |  |
| `$ignore` | **array** | any addresses to not send messages to |
| `$modified` | **bool** | a marker to indicate that the original object modified by this process |





***

### getAddressesForPrincipal

Returns a list of addresses that are associated with a principal.

```php
protected getAddressesForPrincipal(string $principal): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principal` | **string** |  |





***

### outboxRequest

This method handles POST requests to the schedule-outbox.

```php
public outboxRequest(\Sabre\CalDAV\Schedule\IOutbox $outboxNode, \Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): mixed
```

Currently, two types of requests are supported:
  * FREEBUSY requests from RFC 6638
  * Simple iTIP messages from draft-desruisseaux-caldav-sched-04

The latter is from an expired early draft of the CalDAV scheduling
extensions, but iCal depends on a feature from that spec, so we
implement it.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$outboxNode` | **\Sabre\CalDAV\Schedule\IOutbox** |  |
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### handleFreeBusyRequest

This method is responsible for parsing a free-busy query request and
returning its result in $response.

```php
protected handleFreeBusyRequest(\Sabre\CalDAV\Schedule\IOutbox $outbox, \Sabre\VObject\Component $vObject, \Sabre\HTTP\RequestInterface $request, \Sabre\HTTP\ResponseInterface $response): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$outbox` | **\Sabre\CalDAV\Schedule\IOutbox** |  |
| `$vObject` | **\Sabre\VObject\Component** |  |
| `$request` | **\Sabre\HTTP\RequestInterface** |  |
| `$response` | **\Sabre\HTTP\ResponseInterface** |  |





***

### getFreeBusyForEmail

Returns free-busy information for a specific address. The returned
data is an array containing the following properties:.

```php
protected getFreeBusyForEmail(string $email, \DateTimeInterface $start, \DateTimeInterface $end, \Sabre\VObject\Component $request): array
```

calendar-data : A VFREEBUSY VObject
request-status : an iTip status code.
href: The principal's email address, as requested

The following request status codes may be returned:
  * 2.0;description
  * 3.7;description






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$email` | **string** | address |
| `$start` | **\DateTimeInterface** |  |
| `$end` | **\DateTimeInterface** |  |
| `$request` | **\Sabre\VObject\Component** |  |





***

### scheduleReply

This method checks the 'Schedule-Reply' header
and returns false if it's 'F', otherwise true.

```php
protected scheduleReply(\Sabre\HTTP\RequestInterface $request): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **\Sabre\HTTP\RequestInterface** |  |





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
