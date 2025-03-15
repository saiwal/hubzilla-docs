***

# DB_Upgrade

Upgrade the database schema if necessary.

Compares the currently active database schema version with the version
required for this version of Hubzilla, and performs the upgrade if needed.

If the difference consists of more than one revision of the schema, each of
the intermediate upgrades are performed in turn.

* Full name: `\Zotlabs\Lib\DB_Upgrade`




## Methods


### run

Check the installed and required schema versions and perform the upgrade
if necessary.

```php
public static run(int $db_revision): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$db_revision` | **int** |  |





***


***
> Automatically generated on 2025-03-15
