
# SimplePDO

Simple PDO CalDAV backend.

This class is basically the most minimum example to get a caldav backend up
and running. This class uses the following schema (MySQL example):

CREATE TABLE simple_calendars (
   id INT UNSIGNED NOT NULL PRIMARY KEY AUTO_INCREMENT,
   uri VARBINARY(200) NOT NULL,
   principaluri VARBINARY(200) NOT NULL
);

CREATE TABLE simple_calendarobjects (
   id INT UNSIGNED NOT NULL PRIMARY KEY AUTO_INCREMENT,
   calendarid INT UNSIGNED NOT NULL,
   uri VARBINARY(200) NOT NULL,
   calendardata MEDIUMBLOB
)

To make this class work, you absolutely need to have the PropertyStorage
plugin enabled.

* Full name: `\Sabre\CalDAV\Backend\SimplePDO`
* Parent class: [`\Sabre\CalDAV\Backend\AbstractBackend`](./AbstractBackend.md)



## Properties


### pdo

pdo.

```php
protected \PDO $pdo
```






***

## Methods


### __construct

Creates the backend.

```php
public __construct(\PDO $pdo): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pdo` | **\PDO** |  |





***

### getCalendarsForUser

Returns a list of calendars for a principal.

```php
public getCalendarsForUser(string $principalUri): array
```

Every project is an array with the following keys:
 * id, a unique id that will be used by other functions to modify the
   calendar. This can be the same as the uri or a database key.
 * uri. This is just the 'base uri' or 'filename' of the calendar.
 * principaluri. The owner of the calendar. Almost always the same as
   principalUri passed to this method.

Furthermore it can contain webdav properties in clark notation. A very
common one is '{DAV:}displayname'.

Many clients also require:
{urn:ietf:params:xml:ns:caldav}supported-calendar-component-set
For this property, you can just return an instance of
Sabre\CalDAV\Xml\Property\SupportedCalendarComponentSet.

If you return {http://sabredav.org/ns}read-only and set the value to 1,
ACL will automatically be put in read-only mode.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principalUri` | **string** |  |





***

### createCalendar

Creates a new calendar for a principal.

```php
public createCalendar(string $principalUri, string $calendarUri, array $properties): string
```

If the creation was a success, an id must be returned that can be used
to reference this calendar in other methods, such as updateCalendar.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principalUri` | **string** |  |
| `$calendarUri` | **string** |  |
| `$properties` | **array** |  |





***

### deleteCalendar

Delete a calendar and all it's objects.

```php
public deleteCalendar(string $calendarId): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calendarId` | **string** |  |





***

### getCalendarObjects

Returns all calendar objects within a calendar.

```php
public getCalendarObjects(string $calendarId): array
```

Every item contains an array with the following keys:
  * calendardata - The iCalendar-compatible calendar data
  * uri - a unique key which will be used to construct the uri. This can
    be any arbitrary string, but making sure it ends with '.ics' is a
    good idea. This is only the basename, or filename, not the full
    path.
  * lastmodified - a timestamp of the last modification time
  * etag - An arbitrary string, surrounded by double-quotes. (e.g.:
  '  "abcdef"')
  * size - The size of the calendar objects, in bytes.
  * component - optional, a string containing the type of object, such
    as 'vevent' or 'vtodo'. If specified, this will be used to populate
    the Content-Type header.

Note that the etag is optional, but it's highly encouraged to return for
speed reasons.

The calendardata is also optional. If it's not returned
'getCalendarObject' will be called later, which *is* expected to return
calendardata.

If neither etag or size are specified, the calendardata will be
used/fetched to determine these numbers. If both are specified the
amount of times this is needed is reduced by a great degree.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calendarId` | **string** |  |





***

### getCalendarObject

Returns information from a single calendar object, based on it's object
uri.

```php
public getCalendarObject(string $calendarId, string $objectUri): array|null
```

The object uri is only the basename, or filename and not a full path.

The returned array must have the same keys as getCalendarObjects. The
'calendardata' object is required here though, while it's not required
for getCalendarObjects.

This method must return null if the object did not exist.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calendarId` | **string** |  |
| `$objectUri` | **string** |  |





***

### createCalendarObject

Creates a new calendar object.

```php
public createCalendarObject(mixed $calendarId, string $objectUri, string $calendarData): string|null
```

The object uri is only the basename, or filename and not a full path.

It is possible return an etag from this function, which will be used in
the response to this PUT request. Note that the ETag must be surrounded
by double-quotes.

However, you should only really return this ETag if you don't mangle the
calendar-data. If the result of a subsequent GET to this object is not
the exact same as this request body, you should omit the ETag.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calendarId` | **mixed** |  |
| `$objectUri` | **string** |  |
| `$calendarData` | **string** |  |





***

### updateCalendarObject

Updates an existing calendarobject, based on it's uri.

```php
public updateCalendarObject(mixed $calendarId, string $objectUri, string $calendarData): string|null
```

The object uri is only the basename, or filename and not a full path.

It is possible return an etag from this function, which will be used in
the response to this PUT request. Note that the ETag must be surrounded
by double-quotes.

However, you should only really return this ETag if you don't mangle the
calendar-data. If the result of a subsequent GET to this object is not
the exact same as this request body, you should omit the ETag.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calendarId` | **mixed** |  |
| `$objectUri` | **string** |  |
| `$calendarData` | **string** |  |





***

### deleteCalendarObject

Deletes an existing calendar object.

```php
public deleteCalendarObject(string $calendarId, string $objectUri): mixed
```

The object uri is only the basename, or filename and not a full path.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$calendarId` | **string** |  |
| `$objectUri` | **string** |  |





***


## Inherited methods


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
