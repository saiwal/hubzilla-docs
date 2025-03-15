
# Enotify





* Full name: `\Zotlabs\Lib\Enotify`




## Methods


### submit



```php
public static submit(array $params): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$params` | **array** | an assoziative array with:<br />* \e string \b from_xchan sender xchan hash<br />* \e string \b to_xchan recipient xchan hash<br />* \e array \b item an assoziative array<br />* \e int \b type one of the NOTIFY_* constants from boot.php<br />* \e string \b link<br />* \e string \b parent_mid<br />* \e string \b otype<br />* \e string \b verb<br />* \e string \b activity |





***

### send



```php
public static send(array $params): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$params` | **array** | an assoziative array with:<br />* \e string \b fromName        name of the sender<br />* \e string \b fromEmail       email of the sender<br />* \e string \b replyTo         replyTo address to direct responses<br />* \e string \b toEmail         destination email address<br />* \e string \b messageSubject  subject of the message<br />* \e string \b htmlVersion     html version of the message<br />* \e string \b textVersion     text only version of the message<br />* \e string \b additionalMailHeader  additions to the smtp mail header |





***

### format



```php
public static format(mixed $item): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** |  |





***

### format_notify



```php
public static format_notify(mixed $tt): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tt` | **mixed** |  |





***

### format_intros



```php
public static format_intros(mixed $rr): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rr` | **mixed** |  |





***

### format_files



```php
public static format_files(mixed $rr): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rr` | **mixed** |  |





***

### format_mail



```php
public static format_mail(mixed $rr): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rr` | **mixed** |  |





***

### format_all_events



```php
public static format_all_events(mixed $rr): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rr` | **mixed** |  |





***

### format_register



```php
public static format_register(mixed $rr): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rr` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
