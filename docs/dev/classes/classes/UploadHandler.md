***

# UploadHandler





* Full name: `\UploadHandler`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`IMAGETYPE_GIF`|public| |&#039;image/gif&#039;|
|`IMAGETYPE_JPEG`|public| |&#039;image/jpeg&#039;|
|`IMAGETYPE_PNG`|public| |&#039;image/png&#039;|

## Properties


### options



```php
protected $options
```






***

### error_messages



```php
protected $error_messages
```






***

### image_objects



```php
protected $image_objects
```






***

### response



```php
protected $response
```






***

## Methods


### __construct



```php
public __construct(mixed $options = null, mixed $initialize = true, mixed $error_messages = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **mixed** |  |
| `$initialize` | **mixed** |  |
| `$error_messages` | **mixed** |  |





***

### initialize



```php
protected initialize(): mixed
```












***

### get_full_url



```php
protected get_full_url(): mixed
```












***

### get_user_id



```php
protected get_user_id(): mixed
```












***

### get_user_path



```php
protected get_user_path(): mixed
```












***

### get_upload_path



```php
protected get_upload_path(mixed $file_name = null, mixed $version = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_name` | **mixed** |  |
| `$version` | **mixed** |  |





***

### get_query_separator



```php
protected get_query_separator(mixed $url): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### get_download_url



```php
protected get_download_url(mixed $file_name, mixed $version = null, mixed $direct = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_name` | **mixed** |  |
| `$version` | **mixed** |  |
| `$direct` | **mixed** |  |





***

### set_additional_file_properties



```php
protected set_additional_file_properties(mixed $file): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **mixed** |  |





***

### fix_integer_overflow



```php
protected fix_integer_overflow(mixed $size): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$size` | **mixed** |  |





***

### get_file_size



```php
protected get_file_size(mixed $file_path, mixed $clear_stat_cache = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |
| `$clear_stat_cache` | **mixed** |  |





***

### is_valid_file_object



```php
protected is_valid_file_object(mixed $file_name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_name` | **mixed** |  |





***

### get_file_object



```php
protected get_file_object(mixed $file_name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_name` | **mixed** |  |





***

### get_file_objects



```php
protected get_file_objects(mixed $iteration_method = &#039;get_file_object&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$iteration_method` | **mixed** |  |





***

### count_file_objects



```php
protected count_file_objects(): mixed
```












***

### get_error_message



```php
protected get_error_message(mixed $error): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$error` | **mixed** |  |





***

### get_config_bytes



```php
public get_config_bytes(mixed $val): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$val` | **mixed** |  |





***

### validate_image_file



```php
protected validate_image_file(mixed $uploaded_file, mixed $file, mixed $error, mixed $index): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uploaded_file` | **mixed** |  |
| `$file` | **mixed** |  |
| `$error` | **mixed** |  |
| `$index` | **mixed** |  |





***

### validate



```php
protected validate(mixed $uploaded_file, mixed $file, mixed $error, mixed $index, mixed $content_range): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uploaded_file` | **mixed** |  |
| `$file` | **mixed** |  |
| `$error` | **mixed** |  |
| `$index` | **mixed** |  |
| `$content_range` | **mixed** |  |





***

### upcount_name_callback



```php
protected upcount_name_callback(mixed $matches): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **mixed** |  |





***

### upcount_name



```php
protected upcount_name(mixed $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |





***

### get_unique_filename



```php
protected get_unique_filename(mixed $file_path, mixed $name, mixed $size, mixed $type, mixed $error, mixed $index, mixed $content_range): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |
| `$name` | **mixed** |  |
| `$size` | **mixed** |  |
| `$type` | **mixed** |  |
| `$error` | **mixed** |  |
| `$index` | **mixed** |  |
| `$content_range` | **mixed** |  |





***

### get_valid_image_extensions



```php
protected get_valid_image_extensions(mixed $file_path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |





***

### fix_file_extension



```php
protected fix_file_extension(mixed $file_path, mixed $name, mixed $size, mixed $type, mixed $error, mixed $index, mixed $content_range): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |
| `$name` | **mixed** |  |
| `$size` | **mixed** |  |
| `$type` | **mixed** |  |
| `$error` | **mixed** |  |
| `$index` | **mixed** |  |
| `$content_range` | **mixed** |  |





***

### trim_file_name



```php
protected trim_file_name(mixed $file_path, mixed $name, mixed $size, mixed $type, mixed $error, mixed $index, mixed $content_range): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |
| `$name` | **mixed** |  |
| `$size` | **mixed** |  |
| `$type` | **mixed** |  |
| `$error` | **mixed** |  |
| `$index` | **mixed** |  |
| `$content_range` | **mixed** |  |





***

### get_file_name



```php
protected get_file_name(mixed $file_path, mixed $name, mixed $size, mixed $type, mixed $error, mixed $index, mixed $content_range): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |
| `$name` | **mixed** |  |
| `$size` | **mixed** |  |
| `$type` | **mixed** |  |
| `$error` | **mixed** |  |
| `$index` | **mixed** |  |
| `$content_range` | **mixed** |  |





***

### get_scaled_image_file_paths



```php
protected get_scaled_image_file_paths(mixed $file_name, mixed $version): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_name` | **mixed** |  |
| `$version` | **mixed** |  |





***

### gd_get_image_object



```php
protected gd_get_image_object(mixed $file_path, mixed $func, mixed $no_cache = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |
| `$func` | **mixed** |  |
| `$no_cache` | **mixed** |  |





***

### gd_set_image_object



```php
protected gd_set_image_object(mixed $file_path, mixed $image): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |
| `$image` | **mixed** |  |





***

### gd_destroy_image_object



```php
protected gd_destroy_image_object(mixed $file_path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |





***

### gd_imageflip



```php
protected gd_imageflip(mixed $image, mixed $mode): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$image` | **mixed** |  |
| `$mode` | **mixed** |  |





***

### gd_orient_image



```php
protected gd_orient_image(mixed $file_path, mixed $src_img): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |
| `$src_img` | **mixed** |  |





***

### gd_create_scaled_image



```php
protected gd_create_scaled_image(mixed $file_name, mixed $version, mixed $options): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_name` | **mixed** |  |
| `$version` | **mixed** |  |
| `$options` | **mixed** |  |





***

### imagick_get_image_object



```php
protected imagick_get_image_object(mixed $file_path, mixed $no_cache = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |
| `$no_cache` | **mixed** |  |





***

### imagick_set_image_object



```php
protected imagick_set_image_object(mixed $file_path, mixed $image): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |
| `$image` | **mixed** |  |





***

### imagick_destroy_image_object



```php
protected imagick_destroy_image_object(mixed $file_path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |





***

### imagick_orient_image



```php
protected imagick_orient_image(mixed $image): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$image` | **mixed** |  |





***

### imagick_create_scaled_image



```php
protected imagick_create_scaled_image(mixed $file_name, mixed $version, mixed $options): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_name` | **mixed** |  |
| `$version` | **mixed** |  |
| `$options` | **mixed** |  |





***

### imagemagick_create_scaled_image



```php
protected imagemagick_create_scaled_image(mixed $file_name, mixed $version, mixed $options): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_name` | **mixed** |  |
| `$version` | **mixed** |  |
| `$options` | **mixed** |  |





***

### get_image_size



```php
protected get_image_size(mixed $file_path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |





***

### create_scaled_image



```php
protected create_scaled_image(mixed $file_name, mixed $version, mixed $options): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_name` | **mixed** |  |
| `$version` | **mixed** |  |
| `$options` | **mixed** |  |





***

### destroy_image_object



```php
protected destroy_image_object(mixed $file_path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |





***

### imagetype



```php
protected imagetype(mixed $file_path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |





***

### is_valid_image_file



```php
protected is_valid_image_file(mixed $file_path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |





***

### has_image_file_extension



```php
protected has_image_file_extension(mixed $file_path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |





***

### handle_image_file



```php
protected handle_image_file(mixed $file_path, mixed $file): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |
| `$file` | **mixed** |  |





***

### handle_file_upload



```php
protected handle_file_upload(mixed $uploaded_file, mixed $name, mixed $size, mixed $type, mixed $error, mixed $index = null, mixed $content_range = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$uploaded_file` | **mixed** |  |
| `$name` | **mixed** |  |
| `$size` | **mixed** |  |
| `$type` | **mixed** |  |
| `$error` | **mixed** |  |
| `$index` | **mixed** |  |
| `$content_range` | **mixed** |  |





***

### readfile



```php
protected readfile(mixed $file_path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |





***

### body



```php
protected body(mixed $str): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **mixed** |  |





***

### header



```php
protected header(mixed $str): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **mixed** |  |





***

### get_upload_data



```php
protected get_upload_data(mixed $id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |





***

### get_post_param



```php
protected get_post_param(mixed $id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |





***

### get_query_param



```php
protected get_query_param(mixed $id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |





***

### get_server_var



```php
protected get_server_var(mixed $id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |





***

### handle_form_data



```php
protected handle_form_data(mixed $file, mixed $index): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **mixed** |  |
| `$index` | **mixed** |  |





***

### get_version_param



```php
protected get_version_param(): mixed
```












***

### get_singular_param_name



```php
protected get_singular_param_name(): mixed
```












***

### get_file_name_param



```php
protected get_file_name_param(): mixed
```












***

### get_file_names_params



```php
protected get_file_names_params(): mixed
```












***

### get_file_type



```php
protected get_file_type(mixed $file_path): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file_path` | **mixed** |  |





***

### download



```php
protected download(): mixed
```












***

### send_content_type_header



```php
protected send_content_type_header(): mixed
```












***

### send_access_control_headers



```php
protected send_access_control_headers(): mixed
```












***

### generate_response



```php
public generate_response(mixed $content, mixed $print_response = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$content` | **mixed** |  |
| `$print_response` | **mixed** |  |





***

### get_response



```php
public get_response(): mixed
```












***

### head



```php
public head(): mixed
```












***

### get



```php
public get(mixed $print_response = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$print_response` | **mixed** |  |





***

### post



```php
public post(mixed $print_response = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$print_response` | **mixed** |  |





***

### delete



```php
public delete(mixed $print_response = true): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$print_response` | **mixed** |  |





***

### basename



```php
protected basename(mixed $filepath, mixed $suffix = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filepath` | **mixed** |  |
| `$suffix` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
