
# Connect





* Full name: `\Zotlabs\Lib\Connect`




## Methods


### connect

Takes a $channel and a $url/handle and adds a new connection

```php
public static connect(mixed $channel, mixed $url, mixed $sub_channel = false): mixed
```

Returns array
 $return['success'] boolean true if successful
 $return['abook'] Address book entry joined with xchan if successful
 $return['message'] error text if success is false.

This function does NOT send sync packets to clones. The caller is responsible for doing this

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **mixed** |  |
| `$url` | **mixed** |  |
| `$sub_channel` | **mixed** |  |





***


***
> Automatically generated on 2025-03-19
