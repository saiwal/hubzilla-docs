
# JsonLdTestCase





* Full name: `\JsonLdTestCase`
* Parent class: [`PHPUnit_Framework_TestCase`](./PHPUnit_Framework_TestCase.md)




## Methods


### run

Runs this test case. Overridden to attach to EARL report w/o need for
an external XML configuration file.

```php
public run(\PHPUnit_Framework_TestResult $result = NULL): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$result` | **\PHPUnit_Framework_TestResult** | the test result. |





***

### testExpand

Tests expansion.

```php
public testExpand(\JsonLdTest $test): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\JsonLdTest** | the test to run. |





***

### testCompact

Tests compaction.

```php
public testCompact(\JsonLdTest $test): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\JsonLdTest** | the test to run. |





***

### testFlatten

Tests flatten.

```php
public testFlatten(\JsonLdTest $test): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\JsonLdTest** | the test to run. |





***

### testToRdf

Tests serialization to RDF.

```php
public testToRdf(\JsonLdTest $test): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\JsonLdTest** | the test to run. |





***

### testFromRdf

Tests deserialization from RDF.

```php
public testFromRdf(\JsonLdTest $test): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\JsonLdTest** | the test to run. |





***

### testFrame

Tests framing.

```php
public testFrame(\JsonLdTest $test): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\JsonLdTest** | the test to run. |





***

### testNormalize

Tests normalization.

```php
public testNormalize(\JsonLdTest $test): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\JsonLdTest** | the test to run. |





***

### testUrgna2012

Tests URGNA2012 normalization.

```php
public testUrgna2012(\JsonLdTest $test): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\JsonLdTest** | the test to run. |





***

### testUrdna2015

Tests URDNA2015 normalization.

```php
public testUrdna2015(\JsonLdTest $test): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$test` | **\JsonLdTest** | the test to run. |





***

### expandProvider



```php
public expandProvider(): mixed
```












***

### compactProvider



```php
public compactProvider(): mixed
```












***

### flattenProvider



```php
public flattenProvider(): mixed
```












***

### toRdfProvider



```php
public toRdfProvider(): mixed
```












***

### fromRdfProvider



```php
public fromRdfProvider(): mixed
```












***

### normalizeProvider



```php
public normalizeProvider(): mixed
```












***

### frameProvider



```php
public frameProvider(): mixed
```












***

### urgna2012Provider



```php
public urgna2012Provider(): mixed
```












***

### urdna2015Provider



```php
public urdna2015Provider(): mixed
```












***


***
> Automatically generated on 2025-03-18
