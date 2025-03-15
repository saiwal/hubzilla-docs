
# MarkdownExtra

Markdown Extra Parser Class



* Full name: `\Michelf\MarkdownExtra`
* Parent class: [`\Michelf\Markdown`](./Markdown.md)



## Properties


### fn_id_prefix

Prefix for footnote ids.

```php
public string $fn_id_prefix
```






***

### fn_link_title

Optional title attribute for footnote links.

```php
public string $fn_link_title
```






***

### fn_link_class

Optional class attribute for footnote links and backlinks.

```php
public string $fn_link_class
```






***

### fn_backlink_class



```php
public string $fn_backlink_class
```






***

### fn_backlink_html

Content to be displayed within footnote backlinks. The default is '↩';
the U+FE0E on the end is a Unicode variant selector used to prevent iOS
from displaying the arrow character as an emoji.

```php
public string $fn_backlink_html
```

Optionally use '^^' and '%%' to refer to the footnote number and
reference number respectively. {@see \Michelf\parseFootnotePlaceholders()}




***

### fn_backlink_title

Optional title and aria-label attributes for footnote backlinks for
added accessibility (to ensure backlink uniqueness).

```php
public string $fn_backlink_title
```

Use '^^' and '%%' to refer to the footnote number and reference number
respectively. {@see \Michelf\parseFootnotePlaceholders()}




***

### fn_backlink_label



```php
public string $fn_backlink_label
```






***

### table_align_class_tmpl

Class name for table cell alignment (%% replaced left/center/right)
For instance: 'go-%%' becomes 'go-left' or 'go-right' or 'go-center'
If empty, the align attribute is used instead of a class name.

```php
public string $table_align_class_tmpl
```






***

### code_class_prefix

Optional class prefix for fenced code block.

```php
public string $code_class_prefix
```






***

### code_attr_on_pre

Class attribute for code blocks goes on the `code` tag;
setting this to true will put attributes on the `pre` tag instead.

```php
public bool $code_attr_on_pre
```






***

### predef_abbr

Predefined abbreviations.

```php
public array $predef_abbr
```






***

### hashtag_protection

Only convert atx-style headers if there's a space between the header and #

```php
public bool $hashtag_protection
```






***

### omit_footnotes

Determines whether footnotes should be appended to the end of the document.

```php
public bool $omit_footnotes
```

If true, footnote html can be retrieved from $this->footnotes_assembled.




***

### footnotes_assembled

After parsing, the HTML for the list of footnotes appears here.

```php
public ?string $footnotes_assembled
```

This is available only if $omit_footnotes == true.

Note: when placing the content of `footnotes_assembled` on the page,
consider adding the attribute `role="doc-endnotes"` to the `div` or
`section` that will enclose the list of footnotes so they are
reachable to accessibility tools the same way they would be with the
default HTML output.




***

### footnotes

Extra variables used during extra transformations.

```php
protected array $footnotes
```






***

### footnotes_ordered



```php
protected array $footnotes_ordered
```






***

### footnotes_ref_count



```php
protected array $footnotes_ref_count
```






***

### footnotes_numbers



```php
protected array $footnotes_numbers
```






***

### abbr_desciptions



```php
protected array $abbr_desciptions
```






***

### abbr_word_re



```php
protected string $abbr_word_re
```






***

### footnote_counter

Give the current footnote number.

```php
protected int $footnote_counter
```






***

### ref_attr

Ref attribute for links

```php
protected array $ref_attr
```






***

### id_class_attr_catch_re

Expression to use to catch attributes (includes the braces)

```php
protected string $id_class_attr_catch_re
```






***

### id_class_attr_nocatch_re

Expression to use when parsing in a context when no capture is desired

```php
protected string $id_class_attr_nocatch_re
```






***

### block_tags_re

Tags that are always treated as block tags

```php
protected string $block_tags_re
```






***

### context_block_tags_re

Tags treated as block tags only if the opening tag is alone on its line

```php
protected string $context_block_tags_re
```






***

### contain_span_tags_re

Tags where markdown="1" default to span mode:

```php
protected string $contain_span_tags_re
```






***

### clean_tags_re

Tags which must not have their contents modified, no matter where
they appear

```php
protected string $clean_tags_re
```






***

### auto_close_tags_re

Tags that do not need to be closed.

```php
protected string $auto_close_tags_re
```






***

### em_relist

Redefining emphasis markers so that emphasis by underscore does not
work in the middle of a word.

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

## Methods


### __construct

Constructor function. Initialize the parser object.

```php
public __construct(): void
```












***

### setup

Setting up Extra-specific variables.

```php
protected setup(): void
```












***

### teardown

Clearing Extra-specific variables.

```php
protected teardown(): void
```












***

### doExtraAttributes

Parse attributes caught by the $this->id_class_attr_catch_re expression
and return the HTML-formatted list of attributes.

```php
protected doExtraAttributes(string $tag_name, string $attr, mixed $defaultIdValue = null, array $classes = array()): string
```

Currently supported attributes are .class and #id.

In addition, this method also supports supplying a default Id value,
which will be used to populate the id attribute in case it was not
overridden.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag_name` | **string** |  |
| `$attr` | **string** |  |
| `$defaultIdValue` | **mixed** |  |
| `$classes` | **array** |  |





***

### stripLinkDefinitions

Strips link definitions from text, stores the URLs and titles in
hash references.

```php
protected stripLinkDefinitions(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _stripLinkDefinitions_callback

Strip link definition callback

```php
protected _stripLinkDefinitions_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### hashHTMLBlocks

Hashify HTML Blocks and "clean tags".

```php
protected hashHTMLBlocks(string $text): string
```

We only want to do this for block-level HTML tags, such as headers,
lists, and tables. That's because we still want to wrap <p>s around
"paragraphs" that are wrapped in non-block-level tags, such as anchors,
phrase emphasis, and spans. The list of tags we're looking for is
hard-coded.

This works by calling _HashHTMLBlocks_InMarkdown, which then calls
_HashHTMLBlocks_InHTML when it encounter block tags. When the markdown="1"
attribute is found within a tag, _HashHTMLBlocks_InHTML calls back
 _HashHTMLBlocks_InMarkdown to handle the Markdown syntax within the tag.
These two functions are calling each other. It's recursive!






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _hashHTMLBlocks_inMarkdown

Parse markdown text, calling _HashHTMLBlocks_InHTML for block tags.

```php
protected _hashHTMLBlocks_inMarkdown(string $text, int $indent, string $enclosing_tag_re = &#039;&#039;, bool $span = false): array
```

*   $indent is the number of space to be ignored when checking for code
    blocks. This is important because if we don't take the indent into
    account, something like this (which looks right) won't work as expected:

    <div>
        <div markdown="1">
        Hello World.  <-- Is this a Markdown code block or text?
        </div>  <-- Is this a Markdown code block or a real tag?
    <div>

    If you don't like this, just don't indent the tag on which
    you apply the markdown="1" attribute.

*   If $enclosing_tag_re is not empty, stops at the first unmatched closing
    tag with that name. Nested tags supported.

*   If $span is true, text inside must treated as span. So any double
    newline will be replaced by a single newline so that it does not create
    paragraphs.

Returns an array of that form: ( processed text , remaining text )






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |
| `$indent` | **int** |  |
| `$enclosing_tag_re` | **string** |  |
| `$span` | **bool** |  |





***

### _hashHTMLBlocks_inHTML

Parse HTML, calling _HashHTMLBlocks_InMarkdown for block tags.

```php
protected _hashHTMLBlocks_inHTML(string $text, string $hash_method, bool $md_attr): array
```

*   Calls $hash_method to convert any blocks.
*   Stops when the first opening tag closes.
*   $md_attr indicate if the use of the `markdown="1"` attribute is allowed.
    (it is not inside clean tags)

Returns an array of that form: ( processed text , remaining text )






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |
| `$hash_method` | **string** |  |
| `$md_attr` | **bool** | Handle `markdown=&quot;1&quot;` attribute |





***

### hashClean

Called whenever a tag must be hashed when a function inserts a "clean" tag
in $text, it passes through this function and is automaticaly escaped,
blocking invalid nested overlap.

```php
protected hashClean(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





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

Callback for reference anchors

```php
protected _doAnchors_reference_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### _doAnchors_inline_callback

Callback for inline anchors

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

Callback for referenced images

```php
protected _doImages_reference_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### _doImages_inline_callback

Callback for inline images

```php
protected _doImages_inline_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### doHeaders

Process markdown headers. Redefined to add ID and class attribute support.

```php
protected doHeaders(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _doHeaders_callback_setext

Callback for setext headers

```php
protected _doHeaders_callback_setext(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### _doHeaders_callback_atx

Callback for atx headers

```php
protected _doHeaders_callback_atx(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### doTables

Form HTML tables.

```php
protected doTables(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _doTable_leadingPipe_callback

Callback for removing the leading pipe for each row

```php
protected _doTable_leadingPipe_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### _doTable_makeAlignAttr

Make the align attribute in a table

```php
protected _doTable_makeAlignAttr(string $alignname): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$alignname` | **string** |  |





***

### _doTable_callback

Calback for processing tables

```php
protected _doTable_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### doDefLists

Form HTML definition lists.

```php
protected doDefLists(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _doDefLists_callback

Callback for processing definition lists

```php
protected _doDefLists_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### processDefListItems

Process the contents of a single definition list, splitting it
into individual term and definition list items.

```php
protected processDefListItems(string $list_str): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$list_str` | **string** |  |





***

### _processDefListItems_callback_dt

Callback for <dt> elements in definition lists

```php
protected _processDefListItems_callback_dt(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### _processDefListItems_callback_dd

Callback for <dd> elements in definition lists

```php
protected _processDefListItems_callback_dd(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### doFencedCodeBlocks

Adding the fenced code block syntax to regular Markdown:

```php
protected doFencedCodeBlocks(string $text): string
```

~~~
Code block
~~~






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _doFencedCodeBlocks_callback

Callback to process fenced code blocks

```php
protected _doFencedCodeBlocks_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### _doFencedCodeBlocks_newlines

Replace new lines in fenced code blocks

```php
protected _doFencedCodeBlocks_newlines(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### formParagraphs

Parse text into paragraphs

```php
protected formParagraphs(string $text, bool $wrap_in_p = true): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** | String to process in paragraphs |
| `$wrap_in_p` | **bool** | Whether paragraphs should be wrapped in &lt;p&gt; tags |


**Return Value:**

HTML output




***

### stripFootnotes

Footnotes - Strips link definitions from text, stores the URLs and
titles in hash references.

```php
protected stripFootnotes(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _stripFootnotes_callback

Callback for stripping footnotes

```php
protected _stripFootnotes_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### doFootnotes

Replace footnote references in $text [^id] with a special text-token
which will be replaced by the actual footnote marker in appendFootnotes.

```php
protected doFootnotes(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### appendFootnotes

Append footnote list to text

```php
protected appendFootnotes(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _doFootnotes

Generates the HTML for footnotes.  Called by appendFootnotes, even if
footnotes are not being appended.

```php
protected _doFootnotes(): void
```












***

### _appendFootnotes_callback

Callback for appending footnotes

```php
protected _appendFootnotes_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### parseFootnotePlaceholders

Build footnote label by evaluating any placeholders.

```php
protected parseFootnotePlaceholders(string $label, int $footnote_number, int $reference_number): string
```

- ^^  footnote number
- %%  footnote reference number (Nth reference to footnote number)






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$label` | **string** |  |
| `$footnote_number` | **int** |  |
| `$reference_number` | **int** |  |





***

### stripAbbreviations

Abbreviations - strips abbreviations from text, stores titles in hash
references.

```php
protected stripAbbreviations(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _stripAbbreviations_callback

Callback for stripping abbreviations

```php
protected _stripAbbreviations_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***

### doAbbreviations

Find defined abbreviations in text and wrap them in <abbr> elements.

```php
protected doAbbreviations(string $text): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$text` | **string** |  |





***

### _doAbbreviations_callback

Callback for processing abbreviations

```php
protected _doAbbreviations_callback(array $matches): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matches` | **array** |  |





***


## Inherited methods


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
