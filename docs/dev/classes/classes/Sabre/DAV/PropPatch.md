
# PropPatch

This class represents a set of properties that are going to be updated.

Usually this is simply a PROPPATCH request, but it can also be used for
internal updates.

Property updates must always be atomic. This means that a property update
must either completely succeed, or completely fail.

* Full name: `\Sabre\DAV\PropPatch`



## Properties


### mutations

Properties that are being updated.

```php
protected array $mutations
```

This is a key-value list. If the value is null, the property is supposed
to be deleted.




***

### result

A list of properties and the result of the update. The result is in the
form of a HTTP status code.

```php
protected array $result
```






***

### propertyUpdateCallbacks

This is the list of callbacks when we're performing the actual update.

```php
protected array $propertyUpdateCallbacks
```






***

### failed

This property will be set to true if the operation failed.

```php
protected bool $failed
```






***

## Methods


### __construct

Constructor.

```php
public __construct(array $mutations): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mutations` | **array** | A list of updates |





***

### handle

Call this function if you wish to handle updating certain properties.

```php
public handle(string|string[] $properties, callable $callback): mixed
```

For instance, your class may be responsible for handling updates for the
{DAV:}displayname property.

In that case, call this method with the first argument
"{DAV:}displayname" and a second argument that's a method that does the
actual updating.

It's possible to specify more than one property as an array.

The callback must return a boolean or an it. If the result is true, the
operation was considered successful. If it's false, it's consided
failed.

If the result is an integer, we'll use that integer as the http status
code associated with the operation.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$properties` | **string&#124;string[]** |  |
| `$callback` | **callable** |  |





***

### handleRemaining

Call this function if you wish to handle _all_ properties that haven't
been handled by anything else yet. Note that you effectively claim with
this that you promise to process _all_ properties that are coming in.

```php
public handleRemaining(callable $callback): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$callback` | **callable** |  |





***

### setResultCode

Sets the result code for one or more properties.

```php
public setResultCode(string|string[] $properties, int $resultCode): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$properties` | **string&#124;string[]** |  |
| `$resultCode` | **int** |  |





***

### setRemainingResultCode

Sets the result code for all properties that did not have a result yet.

```php
public setRemainingResultCode(int $resultCode): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$resultCode` | **int** |  |





***

### getRemainingMutations

Returns the list of properties that don't have a result code yet.

```php
public getRemainingMutations(): string[]
```

This method returns a list of property names, but not its values.










***

### getRemainingValues

Returns the list of properties that don't have a result code yet.

```php
public getRemainingValues(): array
```

This method returns list of properties and their values.










***

### commit

Performs the actual update, and calls all callbacks.

```php
public commit(): bool
```

This method returns true or false depending on if the operation was
successful.










***

### doCallBackSingleProp

Executes a property callback with the single-property syntax.

```php
private doCallBackSingleProp(string $propertyName, callable $callback): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propertyName` | **string** |  |
| `$callback` | **callable** |  |





***

### doCallBackMultiProp

Executes a property callback with the multi-property syntax.

```php
private doCallBackMultiProp(array $propertyList, callable $callback): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$propertyList` | **array** |  |
| `$callback` | **callable** |  |





***

### getResult

Returns the result of the operation.

```php
public getResult(): array
```












***

### getMutations

Returns the full list of mutations.

```php
public getMutations(): array
```












***


***
> Automatically generated on 2025-03-15
