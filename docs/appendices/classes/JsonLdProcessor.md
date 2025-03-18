
# JsonLdProcessor

A JSON-LD processor.



* Full name: `\JsonLdProcessor`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`XSD_BOOLEAN`|public| |&#039;http://www.w3.org/2001/XMLSchema#boolean&#039;|
|`XSD_DOUBLE`|public| |&#039;http://www.w3.org/2001/XMLSchema#double&#039;|
|`XSD_INTEGER`|public| |&#039;http://www.w3.org/2001/XMLSchema#integer&#039;|
|`XSD_STRING`|public| |&#039;http://www.w3.org/2001/XMLSchema#string&#039;|
|`RDF_LIST`|public| |&#039;http://www.w3.org/1999/02/22-rdf-syntax-ns#List&#039;|
|`RDF_FIRST`|public| |&#039;http://www.w3.org/1999/02/22-rdf-syntax-ns#first&#039;|
|`RDF_REST`|public| |&#039;http://www.w3.org/1999/02/22-rdf-syntax-ns#rest&#039;|
|`RDF_NIL`|public| |&#039;http://www.w3.org/1999/02/22-rdf-syntax-ns#nil&#039;|
|`RDF_TYPE`|public| |&#039;http://www.w3.org/1999/02/22-rdf-syntax-ns#type&#039;|
|`RDF_LANGSTRING`|public| |&#039;http://www.w3.org/1999/02/22-rdf-syntax-ns#langString&#039;|
|`MAX_CONTEXT_URLS`|public| |10|

## Properties


### rdfParsers

Processor-specific RDF dataset parsers.

```php
protected $rdfParsers
```






***

## Methods


### __construct

Constructs a JSON-LD processor.

```php
public __construct(): mixed
```












***

### compact

Performs JSON-LD compaction.

```php
public compact(mixed $input, mixed $ctx, \assoc $options): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** | the JSON-LD object to compact. |
| `$ctx` | **mixed** | the context to compact with. |
| `$options` | **\assoc** | the compaction options.<br />[base] the base IRI to use.<br />[compactArrays] true to compact arrays to single values when<br />  appropriate, false not to (default: true).<br />[graph] true to always output a top-level graph (default: false).<br />[skipExpansion] true to assume the input is expanded and skip<br />  expansion, false not to, defaults to false.<br />[activeCtx] true to also return the active context used.<br />[documentLoader(url)] the document loader. |


**Return Value:**

the compacted JSON-LD output.




***

### expand

Performs JSON-LD expansion.

```php
public expand(mixed $input, \assoc $options): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** | the JSON-LD object to expand. |
| `$options` | **\assoc** | the options to use:<br />[base] the base IRI to use.<br />[expandContext] a context to expand with.<br />[keepFreeFloatingNodes] true to keep free-floating nodes,<br />  false not to, defaults to false.<br />[documentLoader(url)] the document loader. |


**Return Value:**

the expanded JSON-LD output.




***

### flatten

Performs JSON-LD flattening.

```php
public flatten(mixed $input, mixed $ctx, \assoc $options): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** | the JSON-LD to flatten. |
| `$ctx` | **mixed** |  |
| `$options` | **\assoc** | the options to use:<br />[base] the base IRI to use.<br />[expandContext] a context to expand with.<br />[documentLoader(url)] the document loader. |


**Return Value:**

the flattened output.




***

### frame

Performs JSON-LD framing.

```php
public frame(mixed $input, \stdClass $frame, mixed $options): \stdClass
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** | the JSON-LD object to frame. |
| `$frame` | **\stdClass** | the JSON-LD frame to use. |
| `$options` | **mixed** | the framing options.<br />[base] the base IRI to use.<br />[expandContext] a context to expand with.<br />[embed] default @embed flag: &#039;@last&#039;, &#039;@always&#039;, &#039;@never&#039;, &#039;@link&#039;<br />  (default: &#039;@last&#039;).<br />[explicit] default @explicit flag (default: false).<br />[requireAll] default @requireAll flag (default: true).<br />[omitDefault] default @omitDefault flag (default: false).<br />[documentLoader(url)] the document loader. |


**Return Value:**

the framed JSON-LD output.




***

### normalize

Performs JSON-LD normalization.

```php
public normalize(mixed $input, \assoc $options): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** | the JSON-LD object to normalize. |
| `$options` | **\assoc** | the options to use:<br />[base] the base IRI to use.<br />[expandContext] a context to expand with.<br />[inputFormat] the format if input is not JSON-LD:<br />  &#039;application/nquads&#039; for N-Quads.<br />[format] the format if output is a string:<br />  &#039;application/nquads&#039; for N-Quads.<br />[documentLoader(url)] the document loader. |


**Return Value:**

the normalized output.




***

### fromRDF

Converts an RDF dataset to JSON-LD.

```php
public fromRDF(mixed $dataset, \assoc $options): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dataset` | **mixed** | a serialized string of RDF in a format specified<br />by the format option or an RDF dataset to convert. |
| `$options` | **\assoc** | the options to use:<br />[format] the format if input is a string:<br />  &#039;application/nquads&#039; for N-Quads (default).<br />[useRdfType] true to use rdf:type, false to use @type<br />  (default: false).<br />[useNativeTypes] true to convert XSD types into native types<br />  (boolean, integer, double), false not to (default: false). |


**Return Value:**

the JSON-LD output.




***

### toRDF

Outputs the RDF dataset found in the given JSON-LD object.

```php
public toRDF(mixed $input, \assoc $options): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** | the JSON-LD object. |
| `$options` | **\assoc** | the options to use:<br />[base] the base IRI to use.<br />[expandContext] a context to expand with.<br />[format] the format to use to output a string:<br />  &#039;application/nquads&#039; for N-Quads.<br />[produceGeneralizedRdf] true to output generalized RDF, false<br />  to produce only standard RDF (default: false).<br />[documentLoader(url)] the document loader. |


**Return Value:**

the resulting RDF dataset (or a serialization of it).




***

### processContext

Processes a local context, resolving any URLs as necessary, and returns a
new active context in its callback.

```php
public processContext(\stdClass $active_ctx, mixed $local_ctx, \assoc $options): \stdClass
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$active_ctx` | **\stdClass** | the current active context. |
| `$local_ctx` | **mixed** | the local context to process. |
| `$options` | **\assoc** | the options to use:<br />[documentLoader(url)] the document loader. |


**Return Value:**

the new active context.




***

### hasProperty

Returns true if the given subject has the given property.

```php
public static hasProperty(\stdClass $subject, string $property): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$subject` | **\stdClass** | the subject to check. |
| `$property` | **string** | the property to look for. |


**Return Value:**

true if the subject has the given property, false if not.




***

### hasValue

Determines if the given value is a property of the given subject.

```php
public static hasValue(\stdClass $subject, string $property, mixed $value): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$subject` | **\stdClass** | the subject to check. |
| `$property` | **string** | the property to check. |
| `$value` | **mixed** | the value to check. |


**Return Value:**

true if the value exists, false if not.




***

### addValue

Adds a value to a subject. If the value is an array, all values in the
array will be added.

```php
public static addValue(\stdClass $subject, string $property, mixed $value, mixed $options = array()): mixed
```

Note: If the value is a subject that already exists as a property of the
given subject, this method makes no attempt to deeply merge properties.
Instead, the value will not be added.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$subject` | **\stdClass** | the subject to add the value to. |
| `$property` | **string** | the property that relates the value to the subject. |
| `$value` | **mixed** | the value to add. |
| `$options` | **mixed** |  |





***

### getValues

Gets all of the values for a subject's property as an array.

```php
public static getValues(\stdClass $subject, string $property): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$subject` | **\stdClass** | the subject. |
| `$property` | **string** | the property. |


**Return Value:**

all of the values for a subject's property as an array.




***

### removeProperty

Removes a property from a subject.

```php
public static removeProperty(\stdClass $subject, string $property): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$subject` | **\stdClass** | the subject. |
| `$property` | **string** | the property. |





***

### removeValue

Removes a value from a subject.

```php
public static removeValue(\stdClass $subject, string $property, mixed $value, mixed $options = array()): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$subject` | **\stdClass** | the subject. |
| `$property` | **string** | the property that relates the value to the subject. |
| `$value` | **mixed** | the value to remove. |
| `$options` | **mixed** |  |





***

### compareValues

Compares two JSON-LD values for equality. Two JSON-LD values will be
considered equal if:

```php
public static compareValues(mixed $v1, mixed $v2): bool
```

1. They are both primitives of the same type and value.
2. They are both @values with the same @value, @type, @language,
  and @index, OR
3. They both have @ids that are the same.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$v1` | **mixed** | the first value. |
| `$v2` | **mixed** | the second value. |


**Return Value:**

true if v1 and v2 are considered equal, false if not.




***

### getContextValue

Gets the value for the given active context key and type, null if none is
set.

```php
public static getContextValue(\stdClass $ctx, string $key, mixed $type): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ctx` | **\stdClass** | the active context. |
| `$key` | **string** | the context key. |
| `$type` | **mixed** |  |


**Return Value:**

the value.




***

### parseNQuads

Parses RDF in the form of N-Quads.

```php
public static parseNQuads(string $input): \stdClass
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **string** | the N-Quads input to parse. |


**Return Value:**

an RDF dataset.




***

### toNQuads

Converts an RDF dataset to N-Quads.

```php
public static toNQuads(\stdClass $dataset): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dataset` | **\stdClass** | the RDF dataset to convert. |


**Return Value:**

the N-Quads string.




***

### toNQuad

Converts an RDF triple and graph name to an N-Quad string (a single quad).

```php
public static toNQuad(\stdClass $triple, mixed $graph_name, string $bnode = null): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$triple` | **\stdClass** | the RDF triple to convert. |
| `$graph_name` | **mixed** | the name of the graph containing the triple, null<br />for the default graph. |
| `$bnode` | **string** | the bnode the quad is mapped to (optional, for<br />use during normalization only). |


**Return Value:**

the N-Quad string.




***

### registerRDFParser

Registers a processor-specific RDF dataset parser by content-type.

```php
public registerRDFParser(string $content_type, callable $parser): mixed
```

Global parsers will no longer be used by this processor.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$content_type` | **string** | the content-type for the parser. |
| `$parser` | **callable** | (input) the parser function (takes a string as<br />a parameter and returns an RDF dataset). |





***

### unregisterRDFParser

Unregisters a process-specific RDF dataset parser by content-type. If
there are no remaining processor-specific parsers, then the global
parsers will be re-enabled.

```php
public unregisterRDFParser(string $content_type): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$content_type` | **string** | the content-type for the parser. |





***

### arrayify

If $value is an array, returns $value, otherwise returns an array
containing $value as the only element.

```php
public static arrayify(mixed $value): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **mixed** | the value. |


**Return Value:**

an array.




***

### copy

Clones an object, array, or string/number.

```php
public static copy(mixed $value): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **mixed** | the value to clone. |


**Return Value:**

the cloned value.




***

### setdefault

Sets the value of a key for the given array if that property
has not already been set.

```php
public static setdefault(mixed& $arr, string $key, mixed $value): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **mixed** |  |
| `$key` | **string** | the key to update. |
| `$value` | **mixed** | the value to set. |





***

### setdefaults

Sets default values for keys in the given array.

```php
public static setdefaults(mixed& $arr, \assoc $defaults): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arr` | **mixed** |  |
| `$defaults` | **\assoc** | the default keys and values. |





***

### _compact

Recursively compacts an element using the given active context. All values
must be in expanded form before this method is called.

```php
protected _compact(\stdClass $active_ctx, mixed $active_property, mixed $element, \assoc $options): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$active_ctx` | **\stdClass** | the active context to use. |
| `$active_property` | **mixed** | the compacted property with the element<br />to compact, null for none. |
| `$element` | **mixed** | the element to compact. |
| `$options` | **\assoc** | the compaction options. |


**Return Value:**

the compacted value.




***

### _expand

Recursively expands an element using the given context. Any context in
the element will be removed. All context URLs must have been retrieved
before calling this method.

```php
protected _expand(\stdClass $active_ctx, mixed $active_property, mixed $element, \assoc $options, bool $inside_list): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$active_ctx` | **\stdClass** | the active context to use. |
| `$active_property` | **mixed** | the property for the element, null for none. |
| `$element` | **mixed** | the element to expand. |
| `$options` | **\assoc** | the expansion options. |
| `$inside_list` | **bool** | true if the property is a list, false if not. |


**Return Value:**

the expanded value.




***

### _flatten

Performs JSON-LD flattening.

```php
protected _flatten(array $input): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **array** | the expanded JSON-LD to flatten. |


**Return Value:**

the flattened output.




***

### _frame

Performs JSON-LD framing.

```php
protected _frame(array $input, array $frame, \assoc $options): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **array** | the expanded JSON-LD to frame. |
| `$frame` | **array** | the expanded JSON-LD frame to use. |
| `$options` | **\assoc** | the framing options. |


**Return Value:**

the framed output.




***

### _normalize

Performs normalization on the given RDF dataset.

```php
protected _normalize(\stdClass $dataset, \assoc $options): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dataset` | **\stdClass** | the RDF dataset to normalize. |
| `$options` | **\assoc** | the normalization options. |


**Return Value:**

the normalized output.




***

### _fromRDF

Converts an RDF dataset to JSON-LD.

```php
protected _fromRDF(\stdClass $dataset, \assoc $options): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dataset` | **\stdClass** | the RDF dataset. |
| `$options` | **\assoc** | the RDF serialization options. |


**Return Value:**

the JSON-LD output.




***

### _processContext

Processes a local context and returns a new active context.

```php
protected _processContext(\stdClass $active_ctx, mixed $local_ctx, \assoc $options): \stdClass
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$active_ctx` | **\stdClass** | the current active context. |
| `$local_ctx` | **mixed** | the local context to process. |
| `$options` | **\assoc** | the context processing options. |


**Return Value:**

the new active context.




***

### _expandLanguageMap

Expands a language map.

```php
protected _expandLanguageMap(\stdClass $language_map): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$language_map` | **\stdClass** | the language map to expand. |


**Return Value:**

the expanded language map.




***

### _labelBlankNodes

Labels the blank nodes in the given value using the given UniqueNamer.

```php
public _labelBlankNodes(\UniqueNamer $namer, mixed $element): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$namer` | **\UniqueNamer** | the UniqueNamer to use. |
| `$element` | **mixed** | the element with blank nodes to rename. |


**Return Value:**

the element.




***

### _expandValue

Expands the given value by using the coercion and keyword rules in the
given context.

```php
protected _expandValue(\stdClass $active_ctx, string $active_property, mixed $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$active_ctx` | **\stdClass** | the active context to use. |
| `$active_property` | **string** | the property the value is associated with. |
| `$value` | **mixed** | the value to expand. |


**Return Value:**

the expanded value.




***

### _graphToRDF

Creates an array of RDF triples for the given graph.

```php
protected _graphToRDF(\stdClass $graph, \UniqueNamer $namer, \assoc $options): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$graph` | **\stdClass** | the graph to create RDF triples for. |
| `$namer` | **\UniqueNamer** | for assigning bnode names. |
| `$options` | **\assoc** | the RDF serialization options. |


**Return Value:**

the array of RDF triples for the given graph.




***

### _listToRDF

Converts a @list value into linked list of blank node RDF triples
(an RDF collection).

```php
protected _listToRDF(array $list, \UniqueNamer $namer, \stdClass $subject, \stdClass $predicate, mixed& $triples): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$list` | **array** | the @list value. |
| `$namer` | **\UniqueNamer** | for assigning blank node names. |
| `$subject` | **\stdClass** | the subject for the head of the list. |
| `$predicate` | **\stdClass** | the predicate for the head of the list. |
| `$triples` | **mixed** |  |





***

### _objectToRDF

Converts a JSON-LD value object to an RDF literal or a JSON-LD string or
node object to an RDF resource.

```php
protected _objectToRDF(mixed $item): \stdClass
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **mixed** | the JSON-LD value or node object. |


**Return Value:**

the RDF literal or RDF resource.




***

### _RDFToObject

Converts an RDF triple object to a JSON-LD object.

```php
protected _RDFToObject(\stdClass $o, bool $use_native_types): \stdClass
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$o` | **\stdClass** | the RDF triple object to convert. |
| `$use_native_types` | **bool** | true to output native types, false not to. |


**Return Value:**

the JSON-LD object.




***

### _createNodeMap

Recursively flattens the subjects in the given JSON-LD expanded input
into a node map.

```php
protected _createNodeMap(mixed $input, \stdClass $graphs, string $graph, \UniqueNamer $namer, mixed $name = null, mixed $list = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** | the JSON-LD expanded input. |
| `$graphs` | **\stdClass** | a map of graph name to subject map. |
| `$graph` | **string** | the name of the current graph. |
| `$namer` | **\UniqueNamer** | the blank node namer. |
| `$name` | **mixed** | the name assigned to the current input if it is a bnode. |
| `$list` | **mixed** | the list to append to, null for none. |





***

### _matchFrame

Frames subjects according to the given frame.

```php
protected _matchFrame(\stdClass $state, array $subjects, array $frame, mixed $parent, mixed $property): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$state` | **\stdClass** | the current framing state. |
| `$subjects` | **array** | the subjects to filter. |
| `$frame` | **array** | the frame. |
| `$parent` | **mixed** | the parent subject or top-level array. |
| `$property` | **mixed** | the parent property, initialized to null. |





***

### _createImplicitFrame

Creates an implicit frame when recursing through subject matches. If
a frame doesn't have an explicit frame for a particular property, then
a wildcard child frame will be created that uses the same flags that the
parent frame used.

```php
public _createImplicitFrame(mixed $flags): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$flags` | **mixed** |  |


**Return Value:**

the implicit frame.




***

### _createsCircularReference

Checks the current subject stack to see if embedding the given subject
would cause a circular reference.

```php
public _createsCircularReference(mixed $subject_to_embed, mixed $subject_stack): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$subject_to_embed` | **mixed** |  |
| `$subject_stack` | **mixed** |  |


**Return Value:**

true if a circular reference would be created, false if not.




***

### _getFrameFlag

Gets the frame flag value for the given flag name.

```php
protected _getFrameFlag(\stdClass $frame, \stdClass $options, string $name): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$frame` | **\stdClass** | the frame. |
| `$options` | **\stdClass** | the framing options. |
| `$name` | **string** | the flag name. |


**Return Value:**

$the flag value.




***

### _validateFrame

Validates a JSON-LD frame, throwing an exception if the frame is invalid.

```php
protected _validateFrame(array $frame): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$frame` | **array** | the frame to validate. |





***

### _filterSubjects

Returns a map of all of the subjects that match a parsed frame.

```php
protected _filterSubjects(\stdClass $state, array $subjects, \stdClass $frame, \assoc $flags): \stdClass
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$state` | **\stdClass** | the current framing state. |
| `$subjects` | **array** | the set of subjects to filter. |
| `$frame` | **\stdClass** | the parsed frame. |
| `$flags` | **\assoc** | the frame flags. |


**Return Value:**

all of the matched subjects.




***

### _filterSubject

Returns true if the given subject matches the given frame.

```php
protected _filterSubject(\stdClass $subject, \stdClass $frame, \assoc $flags): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$subject` | **\stdClass** | the subject to check. |
| `$frame` | **\stdClass** | the frame to check. |
| `$flags` | **\assoc** | the frame flags. |


**Return Value:**

true if the subject matches, false if not.




***

### _removeEmbed

Removes an existing embed.

```php
protected _removeEmbed(\stdClass $state, string $id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$state` | **\stdClass** | the current framing state. |
| `$id` | **string** | the @id of the embed to remove. |





***

### _addFrameOutput

Adds framing output to the given parent.

```php
protected _addFrameOutput(mixed $parent, string $property, mixed $output): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parent` | **mixed** | the parent to add to. |
| `$property` | **string** | the parent property. |
| `$output` | **mixed** | the output to add. |





***

### _removePreserve

Removes the @preserve keywords as the last step of the framing algorithm.

```php
protected _removePreserve(\stdClass $ctx, mixed $input, \assoc $options): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ctx` | **\stdClass** | the active context used to compact the input. |
| `$input` | **mixed** | the framed, compacted output. |
| `$options` | **\assoc** | the compaction options used. |


**Return Value:**

the resulting output.




***

### _compareRDFTriples

Compares two RDF triples for equality.

```php
protected static _compareRDFTriples(\stdClass $t1, \stdClass $t2): true
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$t1` | **\stdClass** | the first triple. |
| `$t2` | **\stdClass** | the second triple. |


**Return Value:**

if the triples are the same, false if not.




***

### _hashQuads

Hashes all of the quads about a blank node.

```php
protected _hashQuads(string $id, \stdClass $bnodes, \UniqueNamer $namer): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** | the ID of the bnode to hash quads for. |
| `$bnodes` | **\stdClass** | the mapping of bnodes to quads. |
| `$namer` | **\UniqueNamer** | the canonical bnode namer. |


**Return Value:**

the new hash.




***

### _hashPaths

Produces a hash for the paths of adjacent bnodes for a bnode,
incorporating all information about its subgraph of bnodes. This
method will recursively pick adjacent bnode permutations that produce the
lexicographically-least 'path' serializations.

```php
protected _hashPaths(string $id, \stdClass $bnodes, \UniqueNamer $namer, \UniqueNamer $path_namer): \stdClass
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$id` | **string** | the ID of the bnode to hash paths for. |
| `$bnodes` | **\stdClass** | the map of bnode quads. |
| `$namer` | **\UniqueNamer** | the canonical bnode namer. |
| `$path_namer` | **\UniqueNamer** | the namer used to assign names to adjacent<br />bnodes. |


**Return Value:**

the hash and path namer used.




***

### _getAdjacentBlankNodeName

A helper function that gets the blank node name from an RDF quad
node (subject or object). If the node is not a blank node or its
value does not match the given blank node ID, it will be returned.

```php
protected _getAdjacentBlankNodeName(\stdClass $node, string $id): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$node` | **\stdClass** | the RDF quad node. |
| `$id` | **string** | the ID of the blank node to look next to. |


**Return Value:**

the adjacent blank node name or null if none was found.




***

### _compareShortestLeast

Compares two strings first based on length and then lexicographically.

```php
protected _compareShortestLeast(string $a, string $b): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$a` | **string** | the first string. |
| `$b` | **string** | the second string. |


**Return Value:**

-1 if a < b, 1 if a > b, 0 if a == b.




***

### _selectTerm

Picks the preferred compaction term from the given inverse context entry.

```php
protected _selectTerm(mixed $active_ctx, mixed $iri, mixed $value, mixed $containers, mixed $type_or_language, mixed $type_or_language_value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$active_ctx` | **mixed** |  |
| `$iri` | **mixed** |  |
| `$value` | **mixed** |  |
| `$containers` | **mixed** |  |
| `$type_or_language` | **mixed** |  |
| `$type_or_language_value` | **mixed** |  |


**Return Value:**

the preferred term.




***

### _compactIri

Compacts an IRI or keyword into a term or prefix if it can be. If the
IRI has an associated value it may be passed.

```php
protected _compactIri(\stdClass $active_ctx, string $iri, mixed $value = null, \assoc $relative_to = array(), bool $reverse = false): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$active_ctx` | **\stdClass** | the active context to use. |
| `$iri` | **string** | the IRI to compact. |
| `$value` | **mixed** | the value to check or null. |
| `$relative_to` | **\assoc** | options for how to compact IRIs:<br />vocab: true to split after @vocab, false not to. |
| `$reverse` | **bool** | true if a reverse property is being compacted, false<br />if not. |


**Return Value:**

the compacted term, prefix, keyword alias, or original IRI.




***

### _compactValue

Performs value compaction on an object with '@value' or '@id' as the only
property.

```php
protected _compactValue(\stdClass $active_ctx, string $active_property, mixed $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$active_ctx` | **\stdClass** | the active context. |
| `$active_property` | **string** | the active property that points to the<br />value. |
| `$value` | **mixed** | the value to compact. |


**Return Value:**

the compaction result.




***

### _createTermDefinition

Creates a term definition during context processing.

```php
protected _createTermDefinition(\stdClass $active_ctx, \stdClass $local_ctx, string $term, \stdClass $defined): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$active_ctx` | **\stdClass** | the current active context. |
| `$local_ctx` | **\stdClass** | the local context being processed. |
| `$term` | **string** | the key in the local context to define the mapping for. |
| `$defined` | **\stdClass** | a map of defining/defined keys to detect cycles<br />and prevent double definitions. |





***

### _expandIri

Expands a string to a full IRI. The string may be a term, a prefix, a
relative IRI, or an absolute IRI. The associated absolute IRI will be
returned.

```php
public _expandIri(\stdClass $active_ctx, string $value, \assoc $relative_to = array(), \stdClass $local_ctx = null, mixed $defined = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$active_ctx` | **\stdClass** | the current active context. |
| `$value` | **string** | the string to expand. |
| `$relative_to` | **\assoc** | options for how to resolve relative IRIs:<br />base: true to resolve against the base IRI, false not to.<br />vocab: true to concatenate after @vocab, false not to. |
| `$local_ctx` | **\stdClass** | the local context being processed (only given<br />if called during document processing). |
| `$defined` | **mixed** |  |


**Return Value:**

the expanded value.




***

### _findContextUrls

Finds all @context URLs in the given JSON-LD input.

```php
protected _findContextUrls(mixed $input, \stdClass $urls, bool $replace, string $base): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** | the JSON-LD input. |
| `$urls` | **\stdClass** | a map of URLs (url =&gt; false/@contexts). |
| `$replace` | **bool** | true to replace the URLs in the given input with<br />the @contexts from the urls map, false not to. |
| `$base` | **string** | the base URL to resolve relative URLs with. |





***

### _retrieveContextUrls

Retrieves external @context URLs using the given document loader. Each
instance of @context in the input that refers to a URL will be replaced
with the JSON @context found at that URL.

```php
protected _retrieveContextUrls(mixed& $input, \stdClass $cycles, callable $load_document, \base $base = &#039;&#039;): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$input` | **mixed** | the JSON-LD input with possible contexts. |
| `$cycles` | **\stdClass** | an object for tracking context cycles. |
| `$load_document` | **callable** | (url) the document loader. |
| `$base` | **\base** | the base URL to resolve relative URLs against. |


**Return Value:**

the result.




***

### _getInitialContext

Gets the initial context.

```php
protected _getInitialContext(\assoc $options): \stdClass
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$options` | **\assoc** | the options to use.<br />base the document base IRI. |


**Return Value:**

the initial context.




***

### _getInverseContext

Generates an inverse context for use in the compaction algorithm, if
not already generated for the given active context.

```php
protected _getInverseContext(\stdClass $active_ctx): \stdClass
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$active_ctx` | **\stdClass** | the active context to use. |


**Return Value:**

the inverse context.




***

### _buildIriMap

Runs a recursive algorithm to build a lookup map for quickly finding
potential CURIEs.

```php
public _buildIriMap(\ArrayObject $iri_map, string $key, int $idx): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$iri_map` | **\ArrayObject** | the map to build. |
| `$key` | **string** | the current key in the map to work on. |
| `$idx` | **int** | the index into the IRI to compare. |





***

### _addPreferredTerm

Adds the term for the given entry if not already added.

```php
public _addPreferredTerm(\stdClass $mapping, string $term, \stdClass $entry, string $type_or_language_value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mapping` | **\stdClass** | the term mapping. |
| `$term` | **string** | the term to add. |
| `$entry` | **\stdClass** | the inverse context type_or_language entry to<br />add to. |
| `$type_or_language_value` | **string** | the key in the entry to add to. |





***

### _cloneActiveContext

Clones an active context, creating a child active context.

```php
protected _cloneActiveContext(mixed $active_ctx): \stdClass
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$active_ctx` | **mixed** |  |


**Return Value:**

a clone (child) of the active context.




***

### _isKeyword

Returns whether or not the given value is a keyword.

```php
protected static _isKeyword(string $v): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$v` | **string** | the value to check. |


**Return Value:**

true if the value is a keyword, false if not.




***

### _isEmptyObject

Returns true if the given value is an empty Object.

```php
protected static _isEmptyObject(mixed $v): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$v` | **mixed** | the value to check. |


**Return Value:**

true if the value is an empty Object, false if not.




***

### _validateTypeValue

Throws an exception if the given value is not a valid @type value.

```php
protected static _validateTypeValue(mixed $v): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$v` | **mixed** | the value to check. |





***

### _isSubject

Returns true if the given value is a subject with properties.

```php
protected static _isSubject(mixed $v): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$v` | **mixed** | the value to check. |


**Return Value:**

true if the value is a subject with properties, false if not.




***

### _isSubjectReference

Returns true if the given value is a subject reference.

```php
protected static _isSubjectReference(mixed $v): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$v` | **mixed** | the value to check. |


**Return Value:**

true if the value is a subject reference, false if not.




***

### _isValue

Returns true if the given value is a @value.

```php
protected static _isValue(mixed $v): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$v` | **mixed** | the value to check. |


**Return Value:**

true if the value is a @value, false if not.




***

### _isList

Returns true if the given value is a @list.

```php
protected static _isList(mixed $v): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$v` | **mixed** | the value to check. |


**Return Value:**

true if the value is a @list, false if not.




***

### _isBlankNode

Returns true if the given value is a blank node.

```php
protected static _isBlankNode(mixed $v): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$v` | **mixed** | the value to check. |


**Return Value:**

true if the value is a blank node, false if not.




***

### _isAbsoluteIri

Returns true if the given value is an absolute IRI, false if not.

```php
protected static _isAbsoluteIri(string $v): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$v` | **string** | the value to check. |


**Return Value:**

true if the value is an absolute IRI, false if not.




***

### _hasKeyValue

Returns true if the given target has the given key and its
value equals is the given value.

```php
protected static _hasKeyValue(\stdClass $target, mixed $key, mixed $value): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$target` | **\stdClass** | the target object. |
| `$key` | **mixed** |  |
| `$value` | **mixed** | the value to check. |


**Return Value:**

true if the target has the given key and its value matches.




***

### _compareKeyValues

Returns true if both of the given objects have the same value for the
given key or if neither of the objects contain the given key.

```php
protected static _compareKeyValues(\stdClass $o1, \stdClass $o2, mixed $key): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$o1` | **\stdClass** | the first object. |
| `$o2` | **\stdClass** | the second object. |
| `$key` | **mixed** |  |


**Return Value:**

true if both objects have the same value for the key or
neither has the key.




***

### _parse_json

Parses JSON and sets an appropriate exception message on error.

```php
protected static _parse_json(string $json): mixed
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$json` | **string** | the JSON to parse. |


**Return Value:**

the parsed JSON object or array.




***


***
> Automatically generated on 2025-03-18
