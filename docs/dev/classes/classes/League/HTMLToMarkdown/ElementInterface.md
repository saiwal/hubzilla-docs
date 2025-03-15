
# ElementInterface





* Full name: `\League\HTMLToMarkdown\ElementInterface`



## Methods


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

### isDescendantOf



```php
public isDescendantOf(string|string[] $tagNames): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tagNames` | **string&#124;string[]** |  |





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

### getSiblingPosition



```php
public getSiblingPosition(): int
```












***

### getChildrenAsString



```php
public getChildrenAsString(): string
```












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


***
> Automatically generated on 2025-03-15
