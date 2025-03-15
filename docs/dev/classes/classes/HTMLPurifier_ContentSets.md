***

# HTMLPurifier_ContentSets





* Full name: `\HTMLPurifier_ContentSets`



## Properties


### info

List of content set strings (pipe separators) indexed by name.

```php
public $info
```






***

### lookup

List of content set lookups (element => true) indexed by name.

```php
public $lookup
```






***

### keys

Synchronized list of defined content sets (keys of info).

```php
protected $keys
```






***

### values

Synchronized list of defined content values (values of info).

```php
protected $values
```






***

## Methods


### __construct

Merges in module's content sets, expands identifiers in the content
sets and populates the keys, values and lookup member variables.

```php
public __construct(\HTMLPurifier_HTMLModule[] $modules): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$modules` | **\HTMLPurifier_HTMLModule[]** | List of HTMLPurifier_HTMLModule |





***

### generateChildDef

Accepts a definition; generates and assigns a ChildDef for it

```php
public generateChildDef(\HTMLPurifier_ElementDef& $def, \HTMLPurifier_HTMLModule $module): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_ElementDef** | HTMLPurifier_ElementDef reference |
| `$module` | **\HTMLPurifier_HTMLModule** | Module that defined the ElementDef |





***

### generateChildDefCallback



```php
public generateChildDefCallback(mixed $matches): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **mixed** |  |





***

### getChildDef

Instantiates a ChildDef based on content_model and content_model_type
member variables in HTMLPurifier_ElementDef

```php
public getChildDef(\HTMLPurifier_ElementDef $def, \HTMLPurifier_HTMLModule $module): \HTMLPurifier_ChildDef
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$def` | **\HTMLPurifier_ElementDef** | HTMLPurifier_ElementDef to have ChildDef extracted |
| `$module` | **\HTMLPurifier_HTMLModule** | Module that defined the ElementDef |


**Return Value:**

corresponding to ElementDef




***

### convertToLookup

Converts a string list of elements separated by pipes into
a lookup array.

```php
protected convertToLookup(string $string): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **string** | List of elements |


**Return Value:**

Lookup array of elements




***


***
> Automatically generated on 2025-03-15
