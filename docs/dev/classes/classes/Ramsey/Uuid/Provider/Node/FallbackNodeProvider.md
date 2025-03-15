***

# FallbackNodeProvider

FallbackNodeProvider retrieves the system node ID by stepping through a list
of providers until a node ID can be obtained



* Full name: `\Ramsey\Uuid\Provider\Node\FallbackNodeProvider`
* This class implements:
[`\Ramsey\Uuid\Provider\NodeProviderInterface`](../NodeProviderInterface.md)



## Properties


### providers



```php
private iterable $providers
```






***

## Methods


### __construct



```php
public __construct(iterable&lt;\Ramsey\Uuid\Provider\NodeProviderInterface&gt; $providers): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$providers` | **iterable<\Ramsey\Uuid\Provider\NodeProviderInterface>** | Array of node providers |





***

### getNode

Returns a node ID

```php
public getNode(): \Ramsey\Uuid\Type\Hexadecimal
```









**Return Value:**

The node ID as a hexadecimal string




***


***
> Automatically generated on 2025-03-15
