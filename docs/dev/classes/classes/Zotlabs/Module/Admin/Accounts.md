***

# Accounts





* Full name: `\Zotlabs\Module\Admin\Accounts`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`MYP`|public| |&#039;ZAR&#039;|
|`VERSION`|public| |&#039;2.0.0&#039;|


## Methods


### post

Handle POST actions on accounts admin page.

```php
public post(): mixed
```












***

### get



```php
public get(): string
```












***

### handle_ajax_request



```php
private handle_ajax_request(): void
```












***

### block_unblock_accounts

Block or unblock accounts given by the `user` and `blocked` POST params.

```php
private block_unblock_accounts(): void
```

The post params `user` and `blocked` must be present and arrays of equal
lengths. The `user` array should contain account id's or the accounts to
process, and the `blocked` array holds a corresponding boolean value to
indicate that the account at the same offset in the `user` array is or is
not blocked.

An account that is _not_ blocked will be blocked, and accounts that _are_
blocked will be unblocked.










***

### delete_accounts

Delete multiple accounts given by the `user` POST param.

```php
private delete_accounts(): void
```












***


***
> Automatically generated on 2025-03-15
