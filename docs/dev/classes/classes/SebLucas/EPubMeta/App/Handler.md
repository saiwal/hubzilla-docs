
# Handler





* Full name: `\SebLucas\EPubMeta\App\Handler`



## Properties


### bookdir



```php
protected string $bookdir
```






***

### rootdir



```php
protected string $rootdir
```






***

### epub



```php
protected ?\SebLucas\EPubMeta\EPub $epub
```






***

### error



```php
protected ?string $error
```






***

## Methods


### __construct



```php
public __construct(string $bookdir): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bookdir` | **string** |  |





***

### handle

Handle request

```php
public handle(mixed $request = null): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$request` | **mixed** | @todo |





***

### searchBookApi

Proxy google requests

```php
protected searchBookApi(string $query): string|false
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$query` | **string** |  |





***

### getEpubData

Get Epub data

```php
protected getEpubData(\SebLucas\EPubMeta\EPub $epub, array&lt;string,string&gt; $data = []): array&lt;string,string&gt;
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$epub` | **\SebLucas\EPubMeta\EPub** |  |
| `$data` | **array<string,string>** |  |





***

### saveEpubData

Save Epub data

```php
protected saveEpubData(\SebLucas\EPubMeta\EPub $epub): \SebLucas\EPubMeta\EPub
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$epub` | **\SebLucas\EPubMeta\EPub** |  |





***

### renameEpubFile

Rename Epub file

```php
protected renameEpubFile(\SebLucas\EPubMeta\EPub $epub): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$epub` | **\SebLucas\EPubMeta\EPub** |  |





***

### renderTemplate

Render template with data

```php
protected renderTemplate(string $template, array&lt;string,string&gt; $data): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$template` | **string** |  |
| `$data` | **array<string,string>** |  |





***


***
> Automatically generated on 2025-03-15
