
# AbstractBackend

Abstract Calendaring backend. Extend this class to create your own backends.

Checkout the BackendInterface for all the methods that must be implemented.

* Full name: `\Sabre\CalDAV\Backend\AbstractBackend`
* This class implements:
[`\Sabre\CalDAV\Backend\BackendInterface`](./BackendInterface.md)
* This class is an **Abstract class**




## Methods


### updateCalendar

Updates properties for a calendar.

```php
public updateCalendar(mixed $calendarId, \Sabre\DAV\PropPatch $propPatch): mixed
```

The list of mutations is stored in a Sabre\DAV\PropPatch object.
To do the actual updates, you must tell this object which properties
you're going to process with the handle() method.

Calling the handle method is like telling the PropPatch object "I
promise I can handle updating this property".

Read the PropPatch documentation for more info and examples.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calendarId` | **mixed** |  |
| `$propPatch` | **\Sabre\DAV\PropPatch** |  |





***

### getMultipleCalendarObjects

Returns a list of calendar objects.

```php
public getMultipleCalendarObjects(mixed $calendarId, array $uris): array
```

This method should work identical to getCalendarObject, but instead
return all the calendar objects in the list as an array.

If the backend supports this, it may allow for some speed-ups.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calendarId` | **mixed** |  |
| `$uris` | **array** |  |





***

### calendarQuery

Performs a calendar-query on the contents of this calendar.

```php
public calendarQuery(mixed $calendarId, array $filters): array
```

The calendar-query is defined in RFC4791 : CalDAV. Using the
calendar-query it is possible for a client to request a specific set of
object, based on contents of iCalendar properties, date-ranges and
iCalendar component types (VTODO, VEVENT).

This method should just return a list of (relative) urls that match this
query.

The list of filters are specified as an array. The exact array is
documented by \Sabre\CalDAV\CalendarQueryParser.

Note that it is extremely likely that getCalendarObject for every path
returned from this method will be called almost immediately after. You
may want to anticipate this to speed up these requests.

This method provides a default implementation, which parses *all* the
iCalendar objects in the specified calendar.

This default may well be good enough for personal use, and calendars
that aren't very large. But if you anticipate high usage, big calendars
or high loads, you are strongly advised to optimize certain paths.

The best way to do so is override this method and to optimize
specifically for 'common filters'.

Requests that are extremely common are:
  * requests for just VEVENTS
  * requests for just VTODO
  * requests with a time-range-filter on either VEVENT or VTODO.

..and combinations of these requests. It may not be worth it to try to
handle every possible situation and just rely on the (relatively
easy to use) CalendarQueryValidator to handle the rest.

Note that especially time-range-filters may be difficult to parse. A
time-range filter specified on a VEVENT must for instance also handle
recurrence rules correctly.
A good example of how to interpret all these filters can also simply
be found in \Sabre\CalDAV\CalendarQueryFilter. This class is as correct
as possible, so it gives you a good idea on what type of stuff you need
to think of.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calendarId` | **mixed** |  |
| `$filters` | **array** |  |





***

### validateFilterForObject

This method validates if a filter (as passed to calendarQuery) matches
the given object.

```php
protected validateFilterForObject(array $object, array $filters): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$object` | **array** |  |
| `$filters` | **array** |  |





***

### getCalendarObjectByUID

Searches through all of a users calendars and calendar objects to find
an object with a specific UID.

```php
public getCalendarObjectByUID(string $principalUri, string $uid): string|null
```

This method should return the path to this object, relative to the
calendar home, so this path usually only contains two parts:

calendarpath/objectpath.ics

If the uid is not found, return null.

This method should only consider * objects that the principal owns, so
any calendars owned by other principals that also appear in this
collection should be ignored.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principalUri` | **string** |  |
| `$uid` | **string** |  |





***


***
> Automatically generated on 2025-03-18
