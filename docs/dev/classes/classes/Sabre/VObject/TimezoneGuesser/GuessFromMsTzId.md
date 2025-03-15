***

# GuessFromMsTzId





* Full name: `\Sabre\VObject\TimezoneGuesser\GuessFromMsTzId`
* This class implements:
[`\Sabre\VObject\TimezoneGuesser\TimezoneGuesser`](./TimezoneGuesser.md)



## Properties


### microsoftExchangeMap

List of microsoft exchange timezone ids.

```php
public static $microsoftExchangeMap
```

Source: http://msdn.microsoft.com/en-us/library/aa563018(loband).aspx

* This property is **static**.


***

## Methods


### guess



```php
public guess(\Sabre\VObject\Component\VTimeZone $vtimezone, bool $throwIfUnsure = false): ?\DateTimeZone
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$vtimezone` | **\Sabre\VObject\Component\VTimeZone** |  |
| `$throwIfUnsure` | **bool** |  |





***


***
> Automatically generated on 2025-03-15
