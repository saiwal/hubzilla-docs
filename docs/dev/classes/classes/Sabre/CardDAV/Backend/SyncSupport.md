***

# SyncSupport

WebDAV-sync support for CardDAV backends.

In order for backends to advertise support for WebDAV-sync, this interface
must be implemented.

Implementing this can result in a significant reduction of bandwidth and CPU
time.

For this to work, you _must_ return a {http://sabredav.org/ns}sync-token
property from getAddressBooksForUser.

* Full name: `\Sabre\CardDAV\Backend\SyncSupport`
* Parent interfaces: [`\Sabre\CardDAV\Backend\BackendInterface`](./BackendInterface.md)


## Methods


### getChangesForAddressBook

The getChanges method returns all the changes that have happened, since
the specified syncToken in the specified address book.

```php
public getChangesForAddressBook(string $addressBookId, string $syncToken, int $syncLevel, int $limit = null): array|null
```

This function should return an array, such as the following:

[
  'syncToken' => 'The current synctoken',
  'added'   => [
     'new.txt',
  ],
  'modified'   => [
     'modified.txt',
  ],
  'deleted' => [
     'foo.php.bak',
     'old.txt'
  ]
];

The returned syncToken property should reflect the *current* syncToken
of the calendar, as reported in the {http://sabredav.org/ns}sync-token
property. This is needed here too, to ensure the operation is atomic.

If the $syncToken argument is specified as null, this is an initial
sync, and all members should be reported.

The modified property is an array of nodenames that have changed since
the last token.

The deleted property is an array with nodenames, that have been deleted
from collection.

The $syncLevel argument is basically the 'depth' of the report. If it's
1, you only have to report changes that happened only directly in
immediate descendants. If it's 2, it should also include changes from
the nodes below the child collections. (grandchildren)

The $limit argument allows a client to specify how many results should
be returned at most. If the limit is not specified, it should be treated
as infinite.

If the limit (infinite or not) is higher than you're willing to return,
you should throw a Sabre\DAV\Exception\TooMuchMatches() exception.

If the syncToken is expired (due to data cleanup) or unknown, you must
return null.

The limit is 'suggestive'. You are free to ignore it.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$addressBookId` | **string** |  |
| `$syncToken` | **string** |  |
| `$syncLevel` | **int** |  |
| `$limit` | **int** |  |





***


## Inherited methods


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
> Automatically generated on 2025-03-15
