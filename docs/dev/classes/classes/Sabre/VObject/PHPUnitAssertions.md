***

# PHPUnitAssertions

PHPUnit Assertions.

This trait can be added to your unittest to make it easier to test iCalendar
and/or vCards.

* Full name: `\Sabre\VObject\PHPUnitAssertions`




## Methods


### assertVObjectEqualsVObject

This method tests whether two vcards or icalendar objects are
semantically identical.

```php
public assertVObjectEqualsVObject(resource|string|\Sabre\VObject\Component $expected, resource|string|\Sabre\VObject\Component $actual, string $message = &#039;&#039;): mixed
```

It supports objects being supplied as strings, streams or
Sabre\VObject\Component instances.

PRODID is removed from both objects as this is often changes and would
just get in the way.

CALSCALE will automatically get removed if it's set to GREGORIAN.

Any property that has the value **ANY** will be treated as a wildcard.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$expected` | **resource&#124;string&#124;\Sabre\VObject\Component** |  |
| `$actual` | **resource&#124;string&#124;\Sabre\VObject\Component** |  |
| `$message` | **string** |  |





***

***
> Automatically generated on 2025-03-15

