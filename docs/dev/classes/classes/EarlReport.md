
# EarlReport





* Full name: `\EarlReport`
* Parent class: [`PHPUnit_Util_Printer`](./PHPUnit_Util_Printer.md)
* This class implements:
[`\PHPUnit_Framework_TestListener`](./PHPUnit_Framework_TestListener.md)




## Methods


### __construct



```php
public __construct(): mixed
```












***

### attach

Attaches to the given test result, if not yet attached.

```php
public attach(\PHPUnit_Framework_Test $result): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$result` | **\PHPUnit_Framework_Test** | the result to attach to. |





***

### addAssertion

Adds an assertion to this EARL report.

```php
public addAssertion(\JsonLdTest $test, bool $passed): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\JsonLdTest** | the JsonLdTest for the assertion is for. |
| `$passed` | **bool** | whether or not the test passed. |





***

### flush

Writes this EARL report to a file.

```php
public flush(): mixed
```












***

### endTest



```php
public endTest(\PHPUnit_Framework_Test $test, mixed $time): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\PHPUnit_Framework_Test** |  |
| `$time` | **mixed** |  |





***

### addError



```php
public addError(\PHPUnit_Framework_Test $test, \Exception $e, mixed $time): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\PHPUnit_Framework_Test** |  |
| `$e` | **\Exception** |  |
| `$time` | **mixed** |  |





***

### addFailure



```php
public addFailure(\PHPUnit_Framework_Test $test, \PHPUnit_Framework_AssertionFailedError $e, mixed $time): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\PHPUnit_Framework_Test** |  |
| `$e` | **\PHPUnit_Framework_AssertionFailedError** |  |
| `$time` | **mixed** |  |





***

### addIncompleteTest



```php
public addIncompleteTest(\PHPUnit_Framework_Test $test, \Exception $e, mixed $time): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\PHPUnit_Framework_Test** |  |
| `$e` | **\Exception** |  |
| `$time` | **mixed** |  |





***

### addRiskyTest



```php
public addRiskyTest(\PHPUnit_Framework_Test $test, \Exception $e, mixed $time): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\PHPUnit_Framework_Test** |  |
| `$e` | **\Exception** |  |
| `$time` | **mixed** |  |





***

### addSkippedTest



```php
public addSkippedTest(\PHPUnit_Framework_Test $test, \Exception $e, mixed $time): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\PHPUnit_Framework_Test** |  |
| `$e` | **\Exception** |  |
| `$time` | **mixed** |  |





***

### startTest



```php
public startTest(\PHPUnit_Framework_Test $test): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\PHPUnit_Framework_Test** |  |





***

### startTestSuite



```php
public startTestSuite(\PHPUnit_Framework_TestSuite $suite): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$suite` | **\PHPUnit_Framework_TestSuite** |  |





***

### endTestSuite



```php
public endTestSuite(\PHPUnit_Framework_TestSuite $suite): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$suite` | **\PHPUnit_Framework_TestSuite** |  |





***


***
> Automatically generated on 2025-03-15
