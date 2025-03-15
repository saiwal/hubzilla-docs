***

# HTML5TreeConstructer





* Full name: `\HTML5TreeConstructer`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`INIT_PHASE`|public| |0|
|`ROOT_PHASE`|public| |1|
|`MAIN_PHASE`|public| |2|
|`END_PHASE`|public| |3|
|`BEFOR_HEAD`|public| |0|
|`IN_HEAD`|public| |1|
|`AFTER_HEAD`|public| |2|
|`IN_BODY`|public| |3|
|`IN_TABLE`|public| |4|
|`IN_CAPTION`|public| |5|
|`IN_CGROUP`|public| |6|
|`IN_TBODY`|public| |7|
|`IN_ROW`|public| |8|
|`IN_CELL`|public| |9|
|`IN_SELECT`|public| |10|
|`AFTER_BODY`|public| |11|
|`IN_FRAME`|public| |12|
|`AFTR_FRAME`|public| |13|
|`SPECIAL`|public| |0|
|`SCOPING`|public| |1|
|`FORMATTING`|public| |2|
|`PHRASING`|public| |3|
|`MARKER`|public| |0|

## Properties


### stack



```php
public $stack
```






***

### phase



```php
private $phase
```






***

### mode



```php
private $mode
```






***

### dom



```php
private $dom
```






***

### foster_parent



```php
private $foster_parent
```






***

### a_formatting



```php
private $a_formatting
```






***

### head_pointer



```php
private $head_pointer
```






***

### form_pointer



```php
private $form_pointer
```






***

### scoping



```php
private $scoping
```






***

### formatting



```php
private $formatting
```






***

### special



```php
private $special
```






***

## Methods


### __construct



```php
public __construct(): mixed
```












***

### emitToken



```php
public emitToken(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### initPhase



```php
private initPhase(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### rootElementPhase



```php
private rootElementPhase(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### mainPhase



```php
private mainPhase(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### beforeHead



```php
private beforeHead(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### inHead



```php
private inHead(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### afterHead



```php
private afterHead(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### inBody



```php
private inBody(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### inTable



```php
private inTable(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### inCaption



```php
private inCaption(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### inColumnGroup



```php
private inColumnGroup(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### inTableBody



```php
private inTableBody(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### inRow



```php
private inRow(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### inCell



```php
private inCell(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### inSelect



```php
private inSelect(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### afterBody



```php
private afterBody(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### inFrameset



```php
private inFrameset(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### afterFrameset



```php
private afterFrameset(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### trailingEndPhase



```php
private trailingEndPhase(mixed $token): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |





***

### insertElement



```php
private insertElement(mixed $token, mixed $append = true, mixed $check = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **mixed** |  |
| `$append` | **mixed** |  |
| `$check` | **mixed** |  |





***

### insertText



```php
private insertText(mixed $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |





***

### insertComment



```php
private insertComment(mixed $data): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$data` | **mixed** |  |





***

### appendToRealParent



```php
private appendToRealParent(mixed $node): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **mixed** |  |





***

### elementInScope



```php
private elementInScope(mixed $el, mixed $table = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$el` | **mixed** |  |
| `$table` | **mixed** |  |





***

### reconstructActiveFormattingElements



```php
private reconstructActiveFormattingElements(): mixed
```












***

### clearTheActiveFormattingElementsUpToTheLastMarker



```php
private clearTheActiveFormattingElementsUpToTheLastMarker(): mixed
```












***

### generateImpliedEndTags



```php
private generateImpliedEndTags(mixed $exclude = array()): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$exclude` | **mixed** |  |





***

### getElementCategory



```php
private getElementCategory(mixed $node): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **mixed** |  |





***

### clearStackToTableContext



```php
private clearStackToTableContext(mixed $elements): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$elements` | **mixed** |  |





***

### resetInsertionMode



```php
private resetInsertionMode(): mixed
```












***

### closeCell



```php
private closeCell(): mixed
```












***

### save



```php
public save(): mixed
```












***


***
> Automatically generated on 2025-03-15
