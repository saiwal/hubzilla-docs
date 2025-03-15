***

# SimplePie_Source

Handles `<atom:source>`



* Full name: `\SimplePie_Source`
* Parent class: [`\SimplePie\Source`](./SimplePie/Source.md)
* **Warning:** this class is **deprecated**. This means that this class will likely be removed in a future version.






## Inherited methods


### __construct



```php
public __construct(mixed $item, mixed $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |
| `$data` | **mixed** |  |





***

### set_registry

Set the Registry into the class

```php
public set_registry(\SimplePie\Registry $registry): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$registry` | **\SimplePie\Registry** |  |





***

### __toString



```php
public __toString(): mixed
```












***

### get_source_tags



```php
public get_source_tags(mixed $namespace, mixed $tag): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$namespace` | **mixed** |  |
| `$tag` | **mixed** |  |





***

### get_base



```php
public get_base(mixed $element = []): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **mixed** |  |





***

### sanitize



```php
public sanitize(mixed $data, mixed $type, mixed $base = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |
| `$type` | **mixed** |  |
| `$base` | **mixed** |  |





***

### get_item



```php
public get_item(): mixed
```












***

### get_title



```php
public get_title(): mixed
```












***

### get_category



```php
public get_category(mixed $key): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** |  |





***

### get_categories



```php
public get_categories(): mixed
```












***

### get_author



```php
public get_author(mixed $key): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** |  |





***

### get_authors



```php
public get_authors(): mixed
```












***

### get_contributor



```php
public get_contributor(mixed $key): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** |  |





***

### get_contributors



```php
public get_contributors(): mixed
```












***

### get_link



```php
public get_link(mixed $key, mixed $rel = &#039;alternate&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** |  |
| `$rel` | **mixed** |  |





***

### get_permalink

Added for parity between the parent-level and the item/entry-level.

```php
public get_permalink(): mixed
```












***

### get_links



```php
public get_links(mixed $rel = &#039;alternate&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rel` | **mixed** |  |





***

### get_description



```php
public get_description(): mixed
```












***

### get_copyright



```php
public get_copyright(): mixed
```












***

### get_language



```php
public get_language(): mixed
```












***

### get_latitude



```php
public get_latitude(): mixed
```












***

### get_longitude



```php
public get_longitude(): mixed
```












***

### get_image_url



```php
public get_image_url(): mixed
```












***


***
> Automatically generated on 2025-03-15
