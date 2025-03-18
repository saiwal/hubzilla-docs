
# Diff





* Full name: `\Diff`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`UNMODIFIED`|public| |0|
|`DELETED`|public| |1|
|`INSERTED`|public| |2|


## Methods


### compare



```php
public static compare(mixed $string1, mixed $string2, mixed $compareCharacters = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string1` | **mixed** |  |
| `$string2` | **mixed** |  |
| `$compareCharacters` | **mixed** |  |





***

### compareFiles



```php
public static compareFiles(mixed $file1, mixed $file2, mixed $compareCharacters = false): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file1` | **mixed** |  |
| `$file2` | **mixed** |  |
| `$compareCharacters` | **mixed** |  |





***

### computeTable



```php
private static computeTable(mixed $sequence1, mixed $sequence2, mixed $start, mixed $end1, mixed $end2): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sequence1` | **mixed** |  |
| `$sequence2` | **mixed** |  |
| `$start` | **mixed** |  |
| `$end1` | **mixed** |  |
| `$end2` | **mixed** |  |





***

### generatePartialDiff



```php
private static generatePartialDiff(mixed $table, mixed $sequence1, mixed $sequence2, mixed $start): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$table` | **mixed** |  |
| `$sequence1` | **mixed** |  |
| `$sequence2` | **mixed** |  |
| `$start` | **mixed** |  |





***

### toString



```php
public static toString(mixed $diff, mixed $separator = &quot;
&quot;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$diff` | **mixed** |  |
| `$separator` | **mixed** |  |





***

### toHTML



```php
public static toHTML(mixed $diff, mixed $separator = &#039;&lt;br&gt;&#039;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$diff` | **mixed** |  |
| `$separator` | **mixed** |  |





***

### toTable



```php
public static toTable(mixed $diff, mixed $indentation = &#039;&#039;, mixed $separator = &#039;&lt;br&gt;&#039;): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$diff` | **mixed** |  |
| `$indentation` | **mixed** |  |
| `$separator` | **mixed** |  |





***

### getCellContent



```php
private static getCellContent(mixed $diff, mixed $indentation, mixed $separator, mixed& $index, mixed $type): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$diff` | **mixed** |  |
| `$indentation` | **mixed** |  |
| `$separator` | **mixed** |  |
| `$index` | **mixed** |  |
| `$type` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
