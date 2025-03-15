
# Markdown

Markdown Parser Class



* Full name: `\Michelf\Markdown`
* This class implements:
[`\Michelf\MarkdownInterface`](./MarkdownInterface.md)


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`MARKDOWNLIB_VERSION`|public|string|&quot;2.0.0&quot;|

## Properties


### empty_element_suffix

Change to ">" for HTML output.

```php
public string $empty_element_suffix
```






***

### tab_width

The width of indentation of the output markup

```php
public int $tab_width
```






***

### no_markup

Change to `true` to disallow markup or entities.

```php
public bool $no_markup
```






***

### no_entities



```php
public bool $no_entities
```






***

### hard_wrap

Change to `true` to enable line breaks on \n without two trailling spaces

```php
public bool $hard_wrap
```






***

### predef_urls

Predefined URLs and titles for reference links and images.

```php
public array $predef_urls
```






***

### predef_titles



```php
public array $predef_titles
```






***

### url_filter_func

Optional filter function for URLs

```php
public callable|null $url_filter_func
```






***

### header_id_func

Optional header id="" generation callback function.

```php
public callable|null $header_id_func
```






***

### code_block_content_func

Optional function for converting code block content to HTML

```php
public callable|null $code_block_content_func
```






***

### code_span_content_func

Optional function for converting code span content to HTML.

```php
public callable|null $code_span_content_func
```






***

### enhanced_ordered_list

Class attribute to toggle "enhanced ordered list" behaviour
setting this to true will allow ordered lists to start from the index
number that is defined first.

```php
public bool $enhanced_ordered_list
```

For example:
2. List item two
3. List item three

Becomes:
<ol start="2">
<li>List item two</li>
<li>List item three</li>
</ol>




***

### nested_brackets_depth

Regex to match balanced [brackets].

```php
protected int $nested_brackets_depth
```

Needed to insert a maximum bracked depth while converting to PHP.




***

### nested_brackets_re



```php
protected string $nested_brackets_re
```






***

### nested_url_parenthesis_depth



```php
protected int $nested_url_parenthesis_depth
```






***

### nested_url_parenthesis_re



```php
protected string $nested_url_parenthesis_re
```






***

### escape_chars

Table of hash values for escaped characters:

```php
protected string $escape_chars
```






***

### escape_chars_re



```php
protected string $escape_chars_re
```






***

### urls

Internal hashes used during transformation.

```php
protected array $urls
```






***

### titles



```php
protected array $titles
```






***

### html_hashes



```php
protected array $html_hashes
```






***

### in_anchor

Status flag to avoid invalid nesting.

```php
protected bool $in_anchor
```






***

### in_emphasis_processing

Status flag to avoid invalid nesting.

```php
protected bool $in_emphasis_processing
```






***

### document_gamut

Define the document gamut

```php
protected array $document_gamut
```






***

### block_gamut

Define the block gamut - these are all the transformations that form
block-level tags like paragraphs, headers, and list items.

```php
protected array $block_gamut
```






***

### span_gamut

These are all the transformations that occur *within* block-level
tags like paragraphs, headers, and list items.

```php
protected array $span_gamut
```






***

### list_level

Nesting tracker for list levels

```php
protected int $list_level
```






***

### em_relist

Define the emphasis operators with their regex matches

```php
protected array $em_relist
```






***

### strong_relist

Define the strong operators with their regex matches

```php
protected array $strong_relist
```






***

### em_strong_relist

Define the emphasis + strong operators with their regex matches

```php
protected array $em_strong_relist
```






***

### em_strong_prepared_relist

Container for prepared regular expressions

```php
protected ?array $em_strong_prepared_relist
```






***

### utf8_strlen

String length function for detab. `_initDetab` will create a function to
handle UTF-8 if the default function does not exist.

```php
protected $utf8_strlen
```

can be a string or function




***

## Methods


### defaultTransform

Simple function interface - Initialize the parser and return the result
of its transform method. This will work fine for derived classes too.

```php
public static defaultTransform(string $text): string
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### __construct

Constructor function. Initialize appropriate member variables.

```php
public __construct(): void
```












***

### setup

Called before the transformation process starts to setup parser states.

```php
protected setup(): void
```












***

### teardown

Called after the transformation process to clear any variable which may
be taking up memory unnecessarly.

```php
protected teardown(): void
```












***

### transform

Main function. Performs some preprocessing on the input text and pass
it through the document gamut.

```php
public transform(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### stripLinkDefinitions

Strips link definitions from text, stores the URLs and titles in
hash references

```php
protected stripLinkDefinitions(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _stripLinkDefinitions_callback

The callback to strip link definitions

```php
protected _stripLinkDefinitions_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### hashHTMLBlocks

Hashify HTML blocks

```php
protected hashHTMLBlocks(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _hashHTMLBlocks_callback

The callback for hashing HTML blocks

```php
protected _hashHTMLBlocks_callback(string $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **string** |  |





***

### hashPart

Called whenever a tag must be hashed when a function insert an atomic
element in the text stream. Passing $text to through this function gives
a unique text-token which will be reverted back when calling unhash.

```php
protected hashPart(string $text, string $boundary = &#039;X&#039;): string
```

The $boundary argument specify what character should be used to surround
the token. By convension, "B" is used for block elements that needs not
to be wrapped into paragraph tags at the end, ":" is used for elements
that are word separators and "X" is used in the general case.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |
| `$boundary` | **string** |  |





***

### hashBlock

Shortcut function for hashPart with block-level boundaries.

```php
protected hashBlock(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### runBlockGamut

Run block gamut tranformations.

```php
protected runBlockGamut(string $text): string
```

We need to escape raw HTML in Markdown source before doing anything
else. This need to be done for each block, and not only at the
begining in the Markdown function since hashed blocks can be part of
list items and could have been indented. Indented blocks would have
been seen as a code block in a previous pass of hashHTMLBlocks.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### runBasicBlockGamut

Run block gamut tranformations, without hashing HTML blocks. This is
useful when HTML blocks are known to be already hashed, like in the first
whole-document pass.

```php
protected runBasicBlockGamut(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### doHorizontalRules

Convert horizontal rules

```php
protected doHorizontalRules(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### runSpanGamut

Run span gamut transformations

```php
protected runSpanGamut(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### doHardBreaks

Do hard breaks

```php
protected doHardBreaks(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _doHardBreaks_callback

Trigger part hashing for the hard break (callback method)

```php
protected _doHardBreaks_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### doAnchors

Turn Markdown link shortcuts into XHTML <a> tags.

```php
protected doAnchors(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _doAnchors_reference_callback

Callback method to parse referenced anchors

```php
protected _doAnchors_reference_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### _doAnchors_inline_callback

Callback method to parse inline anchors

```php
protected _doAnchors_inline_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### doImages

Turn Markdown image shortcuts into <img> tags.

```php
protected doImages(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _doImages_reference_callback

Callback to parse references image tags

```php
protected _doImages_reference_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### _doImages_inline_callback

Callback to parse inline image tags

```php
protected _doImages_inline_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### doHeaders

Parse Markdown heading elements to HTML

```php
protected doHeaders(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _doHeaders_callback_setext

Setext header parsing callback

```php
protected _doHeaders_callback_setext(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### _doHeaders_callback_atx

ATX header parsing callback

```php
protected _doHeaders_callback_atx(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### _generateIdFromHeaderValue

If a header_id_func property is set, we can use it to automatically
generate an id attribute.

```php
protected _generateIdFromHeaderValue(string $headerValue): string
```

This method returns a string in the form id="foo", or an empty string
otherwise.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$headerValue` | **string** |  |





***

### doLists

Form HTML ordered (numbered) and unordered (bulleted) lists.

```php
protected doLists(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _doLists_callback

List parsing callback

```php
protected _doLists_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### processListItems

Process the contents of a single ordered or unordered list, splitting it
into individual list items.

```php
protected processListItems(string $list_str, string $marker_any_re): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$list_str` | **string** |  |
| `$marker_any_re` | **string** |  |





***

### _processListItems_callback

List item parsing callback

```php
protected _processListItems_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### doCodeBlocks

Process Markdown `<pre><code>` blocks.

```php
protected doCodeBlocks(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _doCodeBlocks_callback

Code block parsing callback

```php
protected _doCodeBlocks_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### makeCodeSpan

Create a code span markup for $code. Called from handleSpanToken.

```php
protected makeCodeSpan(string $code): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** |  |





***

### prepareItalicsAndBold

Prepare regular expressions for searching emphasis tokens in any
context.

```php
protected prepareItalicsAndBold(): void
```












***

### doItalicsAndBold

Convert Markdown italics (emphasis) and bold (strong) to HTML

```php
protected doItalicsAndBold(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### doBlockQuotes

Parse Markdown blockquotes to HTML

```php
protected doBlockQuotes(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _doBlockQuotes_callback

Blockquote parsing callback

```php
protected _doBlockQuotes_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### _doBlockQuotes_callback2

Blockquote parsing callback

```php
protected _doBlockQuotes_callback2(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### formParagraphs

Parse paragraphs

```php
protected formParagraphs(string $text, bool $wrap_in_p = true): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** | String to process in paragraphs |
| `$wrap_in_p` | **bool** | Whether paragraphs should be wrapped in &lt;p&gt; tags |





***

### encodeAttribute

Encode text for a double-quoted HTML attribute. This function
is *not* suitable for attributes enclosed in single quotes.

```php
protected encodeAttribute(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### encodeURLAttribute

Encode text for a double-quoted HTML attribute containing a URL,
applying the URL filter if set. Also generates the textual
representation for the URL (removing mailto: or tel:) storing it in $text.

```php
protected encodeURLAttribute(string $url, string& $text = null): string
```

This function is *not* suitable for attributes enclosed in single quotes.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** |  |
| `$text` | **string** | Passed by reference |


**Return Value:**

URL




***

### encodeAmpsAndAngles

Smart processing for ampersands and angle brackets that need to
be encoded. Valid character entities are left alone unless the
no-entities mode is set.

```php
protected encodeAmpsAndAngles(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### doAutoLinks

Parse Markdown automatic links to anchor HTML tags

```php
protected doAutoLinks(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _doAutoLinks_url_callback

Parse URL callback

```php
protected _doAutoLinks_url_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### _doAutoLinks_email_callback

Parse email address callback

```php
protected _doAutoLinks_email_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### encodeEntityObfuscatedAttribute

Input: some text to obfuscate, e.g. "mailto:foo@example.com"

```php
protected encodeEntityObfuscatedAttribute(string $text, string& $tail = null, int $head_length): string
```

Output: the same text but with most characters encoded as either a
        decimal or hex entity, in the hopes of foiling most address
        harvesting spam bots. E.g.:

       &#109;&#x61;&#105;&#x6c;&#116;&#x6f;&#58;&#x66;o&#111;
       &#x40;&#101;&#x78;&#97;&#x6d;&#112;&#x6c;&#101;&#46;&#x63;&#111;
       &#x6d;

Note: the additional output $tail is assigned the same value as the
ouput, minus the number of characters specified by $head_length.

Based by a filter by Matthew Wickline, posted to BBEdit-Talk.
With some optimizations by Milian Wolff. Forced encoding of HTML
attribute special characters by Allan Odgaard.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |
| `$tail` | **string** | Passed by reference |
| `$head_length` | **int** |  |





***

### parseSpan

Take the string $str and parse it into tokens, hashing embeded HTML,
escaped characters and handling code spans.

```php
protected parseSpan(string $str): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$str` | **string** |  |





***

### handleSpanToken

Handle $token provided by parseSpan by determining its nature and
returning the corresponding value that should replace it.

```php
protected handleSpanToken(string $token, string& $str): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$token` | **string** |  |
| `$str` | **string** | Passed by reference |





***

### outdent

Remove one level of line-leading tabs or spaces

```php
protected outdent(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### detab

Replace tabs with the appropriate amount of spaces.

```php
protected detab(string $text): string
```

For each line we separate the line in blocks delemited by tab characters.
Then we reconstruct every line by adding the  appropriate number of space
between each blocks.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _detab_callback

Replace tabs callback

```php
protected _detab_callback(string $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **string** |  |





***

### _initDetab

Check for the availability of the function in the `utf8_strlen` property
(initially `mb_strlen`). If the function is not available, create a
function that will loosely count the number of UTF-8 characters with a
regular expression.

```php
protected _initDetab(): void
```












***

### unhash

Swap back in all the tags hashed by _HashHTMLBlocks.

```php
protected unhash(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _unhash_callback

Unhashing callback

```php
protected _unhash_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***


***
> Automatically generated on 2025-03-15
