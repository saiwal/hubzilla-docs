***

# AbstractBackend

CardDAV abstract Backend.

This class serves as a base-class for addressbook backends

This class doesn't do much, but it was added for consistency.

* Full name: `\Sabre\CardDAV\Backend\AbstractBackend`
* This class implements:
[`\Sabre\CardDAV\Backend\BackendInterface`](./BackendInterface.md)
* This class is an **Abstract class**




## Methods


### getMultipleCards

Returns a list of cards.

```php
public getMultipleCards(mixed $addressBookId, array $uris): array
```

This method should work identical to getCard, but instead return all the
cards in the list as an array.

If the backend supports this, it may allow for some speed-ups.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$addressBookId` | **mixed** |  |
| `$uris` | **array** |  |





***


***
> Automatically generated on 2025-03-15
