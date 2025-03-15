***

# INodeByPath

INodeByPath.

This interface adds a tiny bit of functionality to collections.

Getting a node that is deep in the tree normally requires going trough each parent node
which can cause a significant performance overhead.

Implementing this interface allows solving this overhead by directly jumping to the target node.

* Full name: `\Sabre\DAV\INodeByPath`



## Methods


### getNodeForPath

Returns the INode object for the requested path.

```php
public getNodeForPath(string $path): \Sabre\DAV\INode|null
```

In case where this collection can not retrieve the requested node
but also can not determine that the node does not exists,
null should be returned to signal that the caller should fallback
to walking the directory tree.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***


***
> Automatically generated on 2025-03-15
