
# Element





* Full name: `\League\HTMLToMarkdown\Element`
* This class implements:
[`\League\HTMLToMarkdown\ElementInterface`](./ElementInterface.md)



## Properties


### node



```php
protected \DOMNode $node
```






***

### nextCached



```php
private \League\HTMLToMarkdown\ElementInterface|null $nextCached
```






***

### previousSiblingCached



```php
private \DOMNode|null $previousSiblingCached
```






***

## Methods


### __construct



```php
public __construct(\DOMNode $node): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\DOMNode** |  |





***

### isBlock



```php
public isBlock(): bool
```












***

### isText



```php
public isText(): bool
```












***

### isWhitespace



```php
public isWhitespace(): bool
```












***

### getTagName



```php
public getTagName(): string
```












***

### getValue



```php
public getValue(): string
```












***

### hasParent



```php
public hasParent(): bool
```












***

### getParent



```php
public getParent(): ?\League\HTMLToMarkdown\ElementInterface
```












***

### getNextSibling



```php
public getNextSibling(): ?\League\HTMLToMarkdown\ElementInterface
```












***

### getPreviousSibling



```php
public getPreviousSibling(): ?\League\HTMLToMarkdown\ElementInterface
```












***

### hasChildren



```php
public hasChildren(): bool
```












***

### getChildren



```php
public getChildren(): \League\HTMLToMarkdown\ElementInterface[]
```












***

### getNext



```php
public getNext(): ?\League\HTMLToMarkdown\ElementInterface
```












***

### getNextNode



```php
private getNextNode(\DOMNode $node, bool $checkChildren = true): ?\DOMNode
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\DOMNode** |  |
| `$checkChildren` | **bool** |  |





***

### isDescendantOf



```php
public isDescendantOf(string[]|string $tagNames): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tagNames` | **string[]&#124;string** |  |





***

### setFinalMarkdown



```php
public setFinalMarkdown(string $markdown): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$markdown` | **string** |  |





***

### getChildrenAsString



```php
public getChildrenAsString(): string
```












***

### getSiblingPosition



```php
public getSiblingPosition(): int
```












***

### getListItemLevel



```php
public getListItemLevel(): int
```












***

### getAttribute



```php
public getAttribute(string $name): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### equals



```php
public equals(\League\HTMLToMarkdown\ElementInterface $element): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **\League\HTMLToMarkdown\ElementInterface** |  |





***


***
> Automatically generated on 2025-03-15
