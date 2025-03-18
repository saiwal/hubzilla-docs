
# QueueWorker





* Full name: `\Zotlabs\Lib\QueueWorker`



## Properties


### queueworker



```php
public static $queueworker
```



* This property is **static**.


***

### maxworkers



```php
public static $maxworkers
```



* This property is **static**.


***

### workermaxage



```php
public static $workermaxage
```



* This property is **static**.


***

### workersleep



```php
public static $workersleep
```



* This property is **static**.


***

### default_priorities



```php
public static $default_priorities
```



* This property is **static**.


***

### long_running_cmd



```php
public static $long_running_cmd
```



* This property is **static**.


***

## Methods


### Summon



```php
public static Summon(mixed $argv): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$argv` | **mixed** |  |





***

### Release



```php
public static Release(mixed $argv): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$argv` | **mixed** |  |





***

### GetWorkerCount



```php
public static GetWorkerCount(): mixed
```



* This method is **static**.








***

### GetWorkerID



```php
public static GetWorkerID(): mixed
```



* This method is **static**.








***

### getWorkId



```php
private static getWorkId(): mixed
```



* This method is **static**.








***

### Process



```php
public static Process(): mixed
```



* This method is **static**.








***

### ClearQueue



```php
public static ClearQueue(): mixed
```



* This method is **static**.








***

### getUuid



```php
private static getUuid(string $data): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **string** |  |


**Return Value:**

$uuid




***


***
> Automatically generated on 2025-03-18
