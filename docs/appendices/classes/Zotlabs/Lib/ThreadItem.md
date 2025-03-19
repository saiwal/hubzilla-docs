
# ThreadItem

A thread item



* Full name: `\Zotlabs\Lib\ThreadItem`



## Properties


### data



```php
public $data
```






***

### template



```php
private $template
```






***

### comment_box_template



```php
private $comment_box_template
```






***

### commentable



```php
private $commentable
```






***

### reactions



```php
private $reactions
```






***

### toplevel



```php
private $toplevel
```






***

### children



```php
private $children
```






***

### parent



```php
private $parent
```






***

### conversation



```php
private $conversation
```






***

### redirect_url



```php
private $redirect_url
```






***

### owner_url



```php
private $owner_url
```






***

### owner_photo



```php
private $owner_photo
```






***

### owner_name



```php
private $owner_name
```






***

### wall_to_wall



```php
private $wall_to_wall
```






***

### threaded



```php
private $threaded
```






***

### visiting



```php
private $visiting
```






***

### channel



```php
private $channel
```






***

### display_mode



```php
private $display_mode
```






***

### reload



```php
private $reload
```






***

### mid_uuid_map



```php
private $mid_uuid_map
```






***

## Methods


### __construct



```php
public __construct(mixed $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |





***

### get_template_data

Get data in a form usable by a conversation template

```php
public get_template_data(mixed $conv_responses, mixed $mid_uuid_map, mixed $thread_level = 1, mixed $conv_flags = []): mixed
```

Returns:
_ The data requested on success
_ false on failure






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$conv_responses` | **mixed** |  |
| `$mid_uuid_map` | **mixed** |  |
| `$thread_level` | **mixed** |  |
| `$conv_flags` | **mixed** |  |





***

### get_id



```php
public get_id(): mixed
```












***

### get_display_mode



```php
public get_display_mode(): mixed
```












***

### set_display_mode



```php
public set_display_mode(mixed $mode): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mode` | **mixed** |  |





***

### is_threaded



```php
public is_threaded(): mixed
```












***

### set_reload



```php
public set_reload(mixed $val): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$val` | **mixed** |  |





***

### get_reload



```php
public get_reload(): mixed
```












***

### set_commentable



```php
public set_commentable(mixed $val): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$val` | **mixed** |  |





***

### is_commentable



```php
public is_commentable(): mixed
```












***

### add_child

Add a child item

```php
public add_child(mixed $item): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |





***

### get_child

Get a child by its ID

```php
public get_child(mixed $id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |





***

### get_children

Get all our children

```php
public get_children(): mixed
```












***

### set_parent

Set our parent

```php
protected set_parent(mixed $item): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |





***

### remove_parent

Remove our parent

```php
protected remove_parent(): mixed
```












***

### remove_child

Remove a child

```php
public remove_child(mixed $item): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |





***

### get_parent

Get parent item

```php
protected get_parent(): mixed
```












***

### set_conversation

set conversation

```php
public set_conversation(mixed $conv): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$conv` | **mixed** |  |





***

### get_conversation

get conversation

```php
public get_conversation(): mixed
```












***

### get_data

Get raw data

```php
public get_data(): mixed
```

We shouldn't need this










***

### get_data_value

Get a data value

```php
public get_data_value(mixed $name): mixed
```

Returns:
_ value on success
_ false on failure






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |





***

### get_template

Get template

```php
public get_template(): mixed
```












***

### set_template



```php
public set_template(mixed $t): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$t` | **mixed** |  |





***

### is_toplevel

Check if this is a toplevel post

```php
private is_toplevel(): mixed
```












***

### count_descendants

Count the total of our descendants

```php
private count_descendants(): mixed
```












***

### count_unseen_descendants



```php
private count_unseen_descendants(): mixed
```












***

### get_comment_box_template

Get the template for the comment box

```php
private get_comment_box_template(): mixed
```












***

### get_comment_box

Get the comment box

```php
private get_comment_box(): mixed
```

Returns:
_ The comment box string (empty if no comment box)
_ false on failure










***

### get_redirect_url



```php
private get_redirect_url(): mixed
```












***

### check_wall_to_wall

Check if we are a wall to wall or announce item and set the relevant properties

```php
protected check_wall_to_wall(): mixed
```












***

### is_wall_to_wall



```php
private is_wall_to_wall(): mixed
```












***

### get_owner_url



```php
private get_owner_url(): mixed
```












***

### get_owner_photo



```php
private get_owner_photo(): mixed
```












***

### get_owner_name



```php
private get_owner_name(): mixed
```












***

### is_visiting



```php
private is_visiting(): mixed
```












***


***
> Automatically generated on 2025-03-19
