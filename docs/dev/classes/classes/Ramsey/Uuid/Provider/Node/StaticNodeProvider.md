***

# StaticNodeProvider

StaticNodeProvider provides a static node value with the multicast bit set



* Full name: `\Ramsey\Uuid\Provider\Node\StaticNodeProvider`
* This class implements:
[`\Ramsey\Uuid\Provider\NodeProviderInterface`](../NodeProviderInterface.md)

**See Also:**

* http://tools.ietf.org/html/rfc4122#section-4.5 - RFC 4122, § 4.5: Node IDs that Do Not Identify the Host



## Properties


### node



```php
private \Ramsey\Uuid\Type\Hexadecimal $node
```






***

## Methods


### __construct



```php
public __construct(\Ramsey\Uuid\Type\Hexadecimal $node): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\Ramsey\Uuid\Type\Hexadecimal** | The static node value to use |





***

### getNode

Returns a node ID

```php
public getNode(): \Ramsey\Uuid\Type\Hexadecimal
```









**Return Value:**

The node ID as a hexadecimal string




***

### setMulticastBit

Set the multicast bit for the static node value

```php
private setMulticastBit(\Ramsey\Uuid\Type\Hexadecimal $node): \Ramsey\Uuid\Type\Hexadecimal
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\Ramsey\Uuid\Type\Hexadecimal** |  |





***


***
> Automatically generated on 2025-03-15
