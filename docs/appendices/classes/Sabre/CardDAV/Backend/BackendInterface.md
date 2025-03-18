
# BackendInterface

CardDAV Backend Interface.

Any CardDAV backend must implement this interface.

Note that there are references to 'addressBookId' scattered throughout the
class. The value of the addressBookId is completely up to you, it can be any
arbitrary value you can use as an unique identifier.

* Full name: `\Sabre\CardDAV\Backend\BackendInterface`



## Methods


### getAddressBooksForUser

Returns the list of addressbooks for a specific user.

```php
public getAddressBooksForUser(string $principalUri): array
```

Every addressbook should have the following properties:
  id - an arbitrary unique id
  uri - the 'basename' part of the url
  principaluri - Same as the passed parameter

Any additional clark-notation property may be passed besides this. Some
common ones are :
  {DAV:}displayname
  {urn:ietf:params:xml:ns:carddav}addressbook-description
  {http://calendarserver.org/ns/}getctag






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principalUri` | **string** |  |





***

### updateAddressBook

Updates properties for an address book.

```php
public updateAddressBook(string $addressBookId, \Sabre\DAV\PropPatch $propPatch): mixed
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
| `$addressBookId` | **string** |  |
| `$propPatch` | **\Sabre\DAV\PropPatch** |  |





***

### createAddressBook

Creates a new address book.

```php
public createAddressBook(string $principalUri, string $url, array $properties): mixed
```

This method should return the id of the new address book. The id can be
in any format, including ints, strings, arrays or objects.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$principalUri` | **string** |  |
| `$url` | **string** | just the &#039;basename&#039; of the url |
| `$properties` | **array** |  |





***

### deleteAddressBook

Deletes an entire addressbook and all its contents.

```php
public deleteAddressBook(mixed $addressBookId): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$addressBookId` | **mixed** |  |





***

### getCards

Returns all cards for a specific addressbook id.

```php
public getCards(mixed $addressbookId): array
```

This method should return the following properties for each card:
  * carddata - raw vcard data
  * uri - Some unique url
  * lastmodified - A unix timestamp

It's recommended to also return the following properties:
  * etag - A unique etag. This must change every time the card changes.
  * size - The size of the card in bytes.

If these last two properties are provided, less time will be spent
calculating them. If they are specified, you can also ommit carddata.
This may speed up certain requests, especially with large cards.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$addressbookId` | **mixed** |  |





***

### getCard

Returns a specfic card.

```php
public getCard(mixed $addressBookId, string $cardUri): array
```

The same set of properties must be returned as with getCards. The only
exception is that 'carddata' is absolutely required.

If the card does not exist, you must return false.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$addressBookId` | **mixed** |  |
| `$cardUri` | **string** |  |





***

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

### createCard

Creates a new card.

```php
public createCard(mixed $addressBookId, string $cardUri, string $cardData): string|null
```

The addressbook id will be passed as the first argument. This is the
same id as it is returned from the getAddressBooksForUser method.

The cardUri is a base uri, and doesn't include the full path. The
cardData argument is the vcard body, and is passed as a string.

It is possible to return an ETag from this method. This ETag is for the
newly created resource, and must be enclosed with double quotes (that
is, the string itself must contain the double quotes).

You should only return the ETag if you store the carddata as-is. If a
subsequent GET request on the same card does not have the same body,
byte-by-byte and you did return an ETag here, clients tend to get
confused.

If you don't return an ETag, you can just return null.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$addressBookId` | **mixed** |  |
| `$cardUri` | **string** |  |
| `$cardData` | **string** |  |





***

### updateCard

Updates a card.

```php
public updateCard(mixed $addressBookId, string $cardUri, string $cardData): string|null
```

The addressbook id will be passed as the first argument. This is the
same id as it is returned from the getAddressBooksForUser method.

The cardUri is a base uri, and doesn't include the full path. The
cardData argument is the vcard body, and is passed as a string.

It is possible to return an ETag from this method. This ETag should
match that of the updated resource, and must be enclosed with double
quotes (that is: the string itself must contain the actual quotes).

You should only return the ETag if you store the carddata as-is. If a
subsequent GET request on the same card does not have the same body,
byte-by-byte and you did return an ETag here, clients tend to get
confused.

If you don't return an ETag, you can just return null.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$addressBookId` | **mixed** |  |
| `$cardUri` | **string** |  |
| `$cardData` | **string** |  |





***

### deleteCard

Deletes a card.

```php
public deleteCard(mixed $addressBookId, string $cardUri): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$addressBookId` | **mixed** |  |
| `$cardUri` | **string** |  |





***


***
> Automatically generated on 2025-03-18
