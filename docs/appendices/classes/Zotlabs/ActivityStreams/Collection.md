
# Collection





* Full name: `\Zotlabs\ActivityStreams\Collection`
* Parent class: [`\Zotlabs\ActivityStreams\ASObject`](./ASObject.md)



## Properties


### totalItems



```php
public int $totalItems
```






***

### current



```php
public string $current
```






***

### first



```php
public string $first
```






***

### last



```php
public string $last
```






***

### items



```php
public array $items
```






***

### collectionOf



```php
public mixed $collectionOf
```






***

## Methods


### getTotalItems



```php
public getTotalItems(): int
```












***

### setTotalItems



```php
public setTotalItems(mixed $totalItems): \Zotlabs\ActivityStreams\Collection
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$totalItems` | **mixed** |  |





***

### getCurrent



```php
public getCurrent(): string
```












***

### setCurrent



```php
public setCurrent(mixed $current): \Zotlabs\ActivityStreams\Collection
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$current` | **mixed** |  |





***

### getFirst



```php
public getFirst(): string
```












***

### setFirst



```php
public setFirst(mixed $first): \Zotlabs\ActivityStreams\Collection
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$first` | **mixed** |  |





***

### getLast



```php
public getLast(): string
```












***

### setLast



```php
public setLast(mixed $last): \Zotlabs\ActivityStreams\Collection
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$last` | **mixed** |  |





***

### getItems



```php
public getItems(): array
```












***

### setItems



```php
public setItems(mixed $items): \Zotlabs\ActivityStreams\Collection
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$items` | **mixed** |  |





***

### getCollectionOf



```php
public getCollectionOf(): mixed
```












***

### setCollectionOf



```php
public setCollectionOf(mixed $collectionOf): \Zotlabs\ActivityStreams\Collection
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$collectionOf` | **mixed** |  |





***


## Inherited methods


### __construct



```php
public __construct(mixed $input = null, mixed $strict = false): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** |  |
| `$strict` | **mixed** |  |




**Throws:**
<p>if $strict</p>

- [`UnhandledElementException`](./UnhandledElementException.md)



***

### getDataType



```php
public getDataType(mixed $element, mixed $object = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$element` | **mixed** |  |
| `$object` | **mixed** |  |





***

### toArray



```php
public toArray(): mixed
```












***

### getLdContext



```php
public getLdContext(): mixed
```












***

### setLdContext



```php
public setLdContext(mixed $ldContext): \Zotlabs\Lib\BaseObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ldContext` | **mixed** |  |





***

### getDirectMessage



```php
public getDirectMessage(): mixed
```












***

### setDirectMessage



```php
public setDirectMessage(mixed $directMessage): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$directMessage` | **mixed** |  |





***

### getSignature



```php
public getSignature(): mixed
```












***

### setSignature



```php
public setSignature(mixed $signature): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$signature` | **mixed** |  |





***

### getProof



```php
public getProof(): mixed
```












***

### setProof



```php
public setProof(mixed $proof): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$proof` | **mixed** |  |





***

### getSensitive



```php
public getSensitive(): mixed
```












***

### setSensitive



```php
public setSensitive(mixed $sensitive): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sensitive` | **mixed** |  |





***

### getReplyTo



```php
public getReplyTo(): mixed
```












***

### setReplyTo



```php
public setReplyTo(mixed $replyTo): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$replyTo` | **mixed** |  |





***

### getWall



```php
public getWall(): mixed
```












***

### setWall



```php
public setWall(mixed $wall): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$wall` | **mixed** |  |





***

### getIsContainedConversation



```php
public getIsContainedConversation(): mixed
```












***

### setIsContainedConversation



```php
public setIsContainedConversation(mixed $isContainedConversation): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$isContainedConversation` | **mixed** |  |





***

### getExpires



```php
public getExpires(): mixed
```












***

### setExpires



```php
public setExpires(mixed $expires): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$expires` | **mixed** |  |





***

### getCanReply



```php
public getCanReply(): mixed
```












***

### setCanReply



```php
public setCanReply(mixed $canReply): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$canReply` | **mixed** |  |





***

### getCanSearch



```php
public getCanSearch(): mixed
```












***

### setCanSearch



```php
public setCanSearch(mixed $canSearch): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$canSearch` | **mixed** |  |





***

### getCommentPolicy



```php
public getCommentPolicy(): mixed
```












***

### setCommentPolicy



```php
public setCommentPolicy(mixed $commentPolicy): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$commentPolicy` | **mixed** |  |





***

### getId



```php
public getId(): mixed
```












***

### setId



```php
public setId(mixed $id): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **mixed** |  |





***

### getType



```php
public getType(): mixed
```












***

### setType



```php
public setType(mixed $type): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **mixed** |  |





***

### getAttachment



```php
public getAttachment(): mixed
```












***

### setAttachment



```php
public setAttachment(mixed $attachment): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attachment` | **mixed** |  |





***

### getAttributedTo



```php
public getAttributedTo(): mixed
```












***

### setAttributedTo



```php
public setAttributedTo(mixed $attributedTo): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$attributedTo` | **mixed** |  |





***

### getAudience



```php
public getAudience(): mixed
```












***

### setAudience



```php
public setAudience(mixed $audience): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$audience` | **mixed** |  |





***

### getContent



```php
public getContent(): mixed
```












***

### setContent



```php
public setContent(mixed $content): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$content` | **mixed** |  |





***

### getContext



```php
public getContext(): mixed
```












***

### setContext



```php
public setContext(mixed $context): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$context` | **mixed** |  |





***

### getName



```php
public getName(): mixed
```












***

### setName



```php
public setName(mixed $name): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **mixed** |  |





***

### getEndTime



```php
public getEndTime(): mixed
```












***

### setEndTime



```php
public setEndTime(mixed $endTime): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$endTime` | **mixed** |  |





***

### getGenerator



```php
public getGenerator(): mixed
```












***

### setGenerator



```php
public setGenerator(mixed $generator): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$generator` | **mixed** |  |





***

### getIcon



```php
public getIcon(): mixed
```












***

### setIcon



```php
public setIcon(mixed $icon): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$icon` | **mixed** |  |





***

### getImage



```php
public getImage(): mixed
```












***

### setImage



```php
public setImage(mixed $image): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$image` | **mixed** |  |





***

### getInReplyTo



```php
public getInReplyTo(): mixed
```












***

### setInReplyTo



```php
public setInReplyTo(mixed $inReplyTo): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$inReplyTo` | **mixed** |  |





***

### getLocation



```php
public getLocation(): mixed
```












***

### setLocation



```php
public setLocation(mixed $location): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$location` | **mixed** |  |





***

### getPreview



```php
public getPreview(): mixed
```












***

### setPreview



```php
public setPreview(mixed $preview): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$preview` | **mixed** |  |





***

### getPublished



```php
public getPublished(): mixed
```












***

### setPublished



```php
public setPublished(mixed $published): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$published` | **mixed** |  |





***

### getReplies



```php
public getReplies(): mixed
```












***

### setReplies



```php
public setReplies(mixed $replies): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$replies` | **mixed** |  |





***

### getStartTime



```php
public getStartTime(): mixed
```












***

### setStartTime



```php
public setStartTime(mixed $startTime): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$startTime` | **mixed** |  |





***

### getSummary



```php
public getSummary(): mixed
```












***

### setSummary



```php
public setSummary(mixed $summary): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$summary` | **mixed** |  |





***

### getTag



```php
public getTag(): mixed
```












***

### setTag



```php
public setTag(mixed $tag): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag` | **mixed** |  |





***

### getUpdated



```php
public getUpdated(): mixed
```












***

### setUpdated



```php
public setUpdated(mixed $updated): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$updated` | **mixed** |  |





***

### getUrl



```php
public getUrl(): mixed
```












***

### setUrl



```php
public setUrl(mixed $url): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **mixed** |  |





***

### getTo



```php
public getTo(): mixed
```












***

### setTo



```php
public setTo(mixed $to): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$to` | **mixed** |  |





***

### getBto



```php
public getBto(): mixed
```












***

### setBto



```php
public setBto(mixed $bto): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bto` | **mixed** |  |





***

### getCc



```php
public getCc(): mixed
```












***

### setCc



```php
public setCc(mixed $cc): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cc` | **mixed** |  |





***

### getBcc



```php
public getBcc(): mixed
```












***

### setBcc



```php
public setBcc(mixed $bcc): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bcc` | **mixed** |  |





***

### getMediaType



```php
public getMediaType(): mixed
```












***

### setMediaType



```php
public setMediaType(mixed $mediaType): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mediaType` | **mixed** |  |





***

### getDuration



```php
public getDuration(): mixed
```












***

### setDuration



```php
public setDuration(mixed $duration): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$duration` | **mixed** |  |





***

### getSource



```php
public getSource(): mixed
```












***

### setSource



```php
public setSource(mixed $source): \Zotlabs\ActivityStreams\ASObject
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **mixed** |  |





***


***
> Automatically generated on 2025-03-18
