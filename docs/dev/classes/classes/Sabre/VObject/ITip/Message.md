***

# Message

This class represents an iTip message.

A message holds all the information relevant to the message, including the
object itself.

It should for the most part be treated as immutable.

* Full name: `\Sabre\VObject\ITip\Message`



## Properties


### uid

The object's UID.

```php
public string $uid
```






***

### component

The component type, such as VEVENT.

```php
public string $component
```






***

### method

Contains the ITip method, which is something like REQUEST, REPLY or
CANCEL.

```php
public string $method
```






***

### sequence

The current sequence number for the event.

```php
public int $sequence
```






***

### sender

The senders' email address.

```php
public string $sender
```

Note that this does not imply that this has to be used in a From: field
if the message is sent by email. It may also be populated in Reply-To:
or not at all.




***

### senderName

The name of the sender. This is often populated from a CN parameter from
either the ORGANIZER or ATTENDEE, depending on the message.

```php
public string|null $senderName
```






***

### recipient

The recipient's email address.

```php
public string $recipient
```






***

### recipientName

The name of the recipient. This is usually populated with the CN
parameter from the ATTENDEE or ORGANIZER property, if it's available.

```php
public string|null $recipientName
```






***

### scheduleStatus

After the message has been delivered, this should contain a string such
as : 1.1;Sent or 1.2;Delivered.

```php
public string $scheduleStatus
```

In case of a failure, this will hold the error status code.

See:
http://tools.ietf.org/html/rfc6638#section-7.3




***

### message

The iCalendar / iTip body.

```php
public \Sabre\VObject\Component\VCalendar $message
```






***

### significantChange

This will be set to true, if the iTip broker considers the change
'significant'.

```php
public bool $significantChange
```

In practice, this means that we'll only mark it true, if for instance
DTSTART changed. This allows systems to only send iTip messages when
significant changes happened. This is especially useful for iMip, as
normally a ton of messages may be generated for normal calendar use.

To see the list of properties that are considered 'significant', check
out Sabre\VObject\ITip\Broker::$significantChangeProperties.




***

## Methods


### getScheduleStatus

Returns the schedule status as a string.

```php
public getScheduleStatus(): mixed
```

For example:
1.2







**Return Value:**

bool|string




***


***
> Automatically generated on 2025-03-15
