
# FreeBusyGenerator

This class helps with generating FREEBUSY reports based on existing sets of
objects.

It only looks at VEVENT and VFREEBUSY objects from the sourcedata, and
generates a single VFREEBUSY object.

VFREEBUSY components are described in RFC5545, The rules for what should
go in a single freebusy report is taken from RFC4791, section 7.10.

* Full name: `\Sabre\VObject\FreeBusyGenerator`



## Properties


### objects

Input objects.

```php
protected array $objects
```






***

### start

Start of range.

```php
protected \DateTimeInterface|null $start
```






***

### end

End of range.

```php
protected \DateTimeInterface|null $end
```






***

### baseObject

VCALENDAR object.

```php
protected \Sabre\VObject\Document $baseObject
```






***

### timeZone

Reference timezone.

```php
protected \DateTimeZone $timeZone
```

When we are calculating busy times, and we come across so-called
floating times (times without a timezone), we use the reference timezone
instead.

This is also used for all-day events.

This defaults to UTC.




***

### vavailability

A VAVAILABILITY document.

```php
protected \Sabre\VObject\Document $vavailability
```

If this is set, its information will be included when calculating
freebusy time.




***

## Methods


### __construct

Creates the generator.

```php
public __construct(\DateTimeInterface $start = null, \DateTimeInterface $end = null, mixed $objects = null, \DateTimeZone $timeZone = null): mixed
```

Check the setTimeRange and setObjects methods for details about the
arguments.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$start` | **\DateTimeInterface** |  |
| `$end` | **\DateTimeInterface** |  |
| `$objects` | **mixed** |  |
| `$timeZone` | **\DateTimeZone** |  |





***

### setBaseObject

Sets the VCALENDAR object.

```php
public setBaseObject(\Sabre\VObject\Document $vcalendar): mixed
```

If this is set, it will not be generated for you. You are responsible
for setting things like the METHOD, CALSCALE, VERSION, etc..

The VFREEBUSY object will be automatically added though.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$vcalendar` | **\Sabre\VObject\Document** |  |





***

### setVAvailability

Sets a VAVAILABILITY document.

```php
public setVAvailability(\Sabre\VObject\Document $vcalendar): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$vcalendar` | **\Sabre\VObject\Document** |  |





***

### setObjects

Sets the input objects.

```php
public setObjects(mixed $objects): mixed
```

You must either specify a vcalendar object as a string, or as the parse
Component.
It's also possible to specify multiple objects as an array.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$objects` | **mixed** |  |





***

### setTimeRange

Sets the time range.

```php
public setTimeRange(\DateTimeInterface $start = null, \DateTimeInterface $end = null): mixed
```

Any freebusy object falling outside of this time range will be ignored.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$start` | **\DateTimeInterface** |  |
| `$end` | **\DateTimeInterface** |  |





***

### setTimeZone

Sets the reference timezone for floating times.

```php
public setTimeZone(\DateTimeZone $timeZone): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$timeZone` | **\DateTimeZone** |  |





***

### getResult

Parses the input data and returns a correct VFREEBUSY object, wrapped in
a VCALENDAR.

```php
public getResult(): \Sabre\VObject\Component
```












***

### calculateAvailability

This method takes a VAVAILABILITY component and figures out all the
available times.

```php
protected calculateAvailability(\Sabre\VObject\FreeBusyData $fbData, \Sabre\VObject\Component\VCalendar $vavailability): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fbData` | **\Sabre\VObject\FreeBusyData** |  |
| `$vavailability` | **\Sabre\VObject\Component\VCalendar** |  |





***

### calculateBusy

This method takes an array of iCalendar objects and applies its busy
times on fbData.

```php
protected calculateBusy(\Sabre\VObject\FreeBusyData $fbData, \Sabre\VObject\Component\VCalendar[] $objects): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fbData` | **\Sabre\VObject\FreeBusyData** |  |
| `$objects` | **\Sabre\VObject\Component\VCalendar[]** |  |





***

### generateFreeBusyCalendar

This method takes a FreeBusyData object and generates the VCALENDAR
object associated with it.

```php
protected generateFreeBusyCalendar(\Sabre\VObject\FreeBusyData $fbData): \Sabre\VObject\Component\VCalendar
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fbData` | **\Sabre\VObject\FreeBusyData** |  |





***


***
> Automatically generated on 2025-03-15
