***

# Broker

The ITip\Broker class is a utility class that helps with processing
so-called iTip messages.

iTip is defined in rfc5546, stands for iCalendar Transport-Independent
Interoperability Protocol, and describes the underlying mechanism for
using iCalendar for scheduling for for example through email (also known as
IMip) and CalDAV Scheduling.

This class helps by:

1. Creating individual invites based on an iCalendar event for each
   attendee.
2. Generating invite updates based on an iCalendar update. This may result
   in new invites, updates and cancellations for attendees, if that list
   changed.
3. On the receiving end, it can create a local iCalendar event based on
   a received invite.
4. It can also process an invite update on a local event, ensuring that any
   overridden properties from attendees are retained.
5. It can create a accepted or declined iTip reply based on an invite.
6. It can process a reply from an invite and update an events attendee
    status based on a reply.

* Full name: `\Sabre\VObject\ITip\Broker`



## Properties


### scheduleAgentServerRules

This setting determines whether the rules for the SCHEDULE-AGENT
parameter should be followed.

```php
public bool $scheduleAgentServerRules
```

This is a parameter defined on ATTENDEE properties, introduced by RFC
6638. This parameter allows a caldav client to tell the server 'Don't do
any scheduling operations'.

If this setting is turned on, any attendees with SCHEDULE-AGENT set to
CLIENT will be ignored. This is the desired behavior for a CalDAV
server, but if you're writing an iTip application that doesn't deal with
CalDAV, you may want to ignore this parameter.




***

### significantChangeProperties

The broker will try during 'parseEvent' figure out whether the change
was significant.

```php
public string[] $significantChangeProperties
```

It uses a few different ways to do this. One of these ways is seeing if
certain properties changed values. This list of specified here.

This list is taken from:
* http://tools.ietf.org/html/rfc5546#section-2.1.4




***

## Methods


### processMessage

This method is used to process an incoming itip message.

```php
public processMessage(\Sabre\VObject\ITip\Message $itipMessage, \Sabre\VObject\Component\VCalendar $existingObject = null): \Sabre\VObject\Component\VCalendar|null
```

Examples:

1. A user is an attendee to an event. The organizer sends an updated
meeting using a new iTip message with METHOD:REQUEST. This function
will process the message and update the attendee's event accordingly.

2. The organizer cancelled the event using METHOD:CANCEL. We will update
the users event to state STATUS:CANCELLED.

3. An attendee sent a reply to an invite using METHOD:REPLY. We can
update the organizers event to update the ATTENDEE with its correct
PARTSTAT.

The $existingObject is updated in-place. If there is no existing object
(because it's a new invite for example) a new object will be created.

If an existing object does not exist, and the method was CANCEL or
REPLY, the message effectively gets ignored, and no 'existingObject'
will be created.

The updated $existingObject is also returned from this function.

If the iTip message was not supported, we will always return false.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$itipMessage` | **\Sabre\VObject\ITip\Message** |  |
| `$existingObject` | **\Sabre\VObject\Component\VCalendar** |  |





***

### parseEvent

This function parses a VCALENDAR object and figure out if any messages
need to be sent.

```php
public parseEvent(\Sabre\VObject\Component\VCalendar|string $calendar, string|array $userHref, \Sabre\VObject\Component\VCalendar|string|null $oldCalendar = null): array
```

A VCALENDAR object will be created from the perspective of either an
attendee, or an organizer. You must pass a string identifying the
current user, so we can figure out who in the list of attendees or the
organizer we are sending this message on behalf of.

It's possible to specify the current user as an array, in case the user
has more than one identifying href (such as multiple emails).

It $oldCalendar is specified, it is assumed that the operation is
updating an existing event, which means that we need to look at the
differences between events, and potentially send old attendees
cancellations, and current attendees updates.

If $calendar is null, but $oldCalendar is specified, we treat the
operation as if the user has deleted an event. If the user was an
organizer, this means that we need to send cancellation notices to
people. If the user was an attendee, we need to make sure that the
organizer gets the 'declined' message.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calendar` | **\Sabre\VObject\Component\VCalendar&#124;string** |  |
| `$userHref` | **string&#124;array** |  |
| `$oldCalendar` | **\Sabre\VObject\Component\VCalendar&#124;string&#124;null** |  |





***

### processMessageRequest

Processes incoming REQUEST messages.

```php
protected processMessageRequest(\Sabre\VObject\ITip\Message $itipMessage, \Sabre\VObject\Component\VCalendar $existingObject = null): \Sabre\VObject\Component\VCalendar|null
```

This is message from an organizer, and is either a new event
invite, or an update to an existing one.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$itipMessage` | **\Sabre\VObject\ITip\Message** |  |
| `$existingObject` | **\Sabre\VObject\Component\VCalendar** |  |





***

### processMessageCancel

Processes incoming CANCEL messages.

```php
protected processMessageCancel(\Sabre\VObject\ITip\Message $itipMessage, \Sabre\VObject\Component\VCalendar $existingObject = null): \Sabre\VObject\Component\VCalendar|null
```

This is a message from an organizer, and means that either an
attendee got removed from an event, or an event got cancelled
altogether.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$itipMessage` | **\Sabre\VObject\ITip\Message** |  |
| `$existingObject` | **\Sabre\VObject\Component\VCalendar** |  |





***

### processMessageReply

Processes incoming REPLY messages.

```php
protected processMessageReply(\Sabre\VObject\ITip\Message $itipMessage, \Sabre\VObject\Component\VCalendar $existingObject = null): \Sabre\VObject\Component\VCalendar|null
```

The message is a reply. This is for example an attendee telling
an organizer he accepted the invite, or declined it.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$itipMessage` | **\Sabre\VObject\ITip\Message** |  |
| `$existingObject` | **\Sabre\VObject\Component\VCalendar** |  |





***

### parseEventForOrganizer

This method is used in cases where an event got updated, and we
potentially need to send emails to attendees to let them know of updates
in the events.

```php
protected parseEventForOrganizer(\Sabre\VObject\Component\VCalendar $calendar, array $eventInfo, array $oldEventInfo): array
```

We will detect which attendees got added, which got removed and create
specific messages for these situations.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calendar` | **\Sabre\VObject\Component\VCalendar** |  |
| `$eventInfo` | **array** |  |
| `$oldEventInfo` | **array** |  |





***

### parseEventForAttendee

Parse an event update for an attendee.

```php
protected parseEventForAttendee(\Sabre\VObject\Component\VCalendar $calendar, array $eventInfo, array $oldEventInfo, string $attendee): \Sabre\VObject\ITip\Message[]
```

This function figures out if we need to send a reply to an organizer.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calendar` | **\Sabre\VObject\Component\VCalendar** |  |
| `$eventInfo` | **array** |  |
| `$oldEventInfo` | **array** |  |
| `$attendee` | **string** |  |





***

### parseEventInfo

Returns attendee information and information about instances of an
event.

```php
protected parseEventInfo(\Sabre\VObject\Component\VCalendar $calendar = null): array
```

Returns an array with the following keys:

1. uid
2. organizer
3. organizerName
4. organizerScheduleAgent
5. organizerForceSend
6. instances
7. attendees
8. sequence
9. exdate
10. timezone - strictly the timezone on which the recurrence rule is
               based on.
11. significantChangeHash
12. status






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calendar` | **\Sabre\VObject\Component\VCalendar** |  |





***


***
> Automatically generated on 2025-03-15
