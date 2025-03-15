***

# Compiler

SCSS compiler



* Full name: `\ScssPhp\ScssPhp\Compiler`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`LINE_COMMENTS`|public| |1|
|`DEBUG_INFO`|public| |2|
|`WITH_RULE`|public| |1|
|`WITH_MEDIA`|public| |2|
|`WITH_SUPPORTS`|public| |4|
|`WITH_ALL`|public| |7|
|`SOURCE_MAP_NONE`|public| |0|
|`SOURCE_MAP_INLINE`|public| |1|
|`SOURCE_MAP_FILE`|public| |2|

## Properties


### operatorNames



```php
protected static array&lt;string,string&gt; $operatorNames
```



* This property is **static**.


***

### namespaces



```php
protected static array&lt;string,string&gt; $namespaces
```



* This property is **static**.


***

### true



```php
public static $true
```



* This property is **static**.


***

### false



```php
public static $false
```



* This property is **static**.


***

### NaN



```php
public static $NaN
```



* This property is **static**.
* **Warning:** this property is **deprecated**. This means that this property will likely be removed in a future version.



***

### Infinity



```php
public static $Infinity
```



* This property is **static**.
* **Warning:** this property is **deprecated**. This means that this property will likely be removed in a future version.



***

### null



```php
public static $null
```



* This property is **static**.


***

### emptyList



```php
public static $emptyList
```



* This property is **static**.


***

### emptyMap



```php
public static $emptyMap
```



* This property is **static**.


***

### emptyString



```php
public static $emptyString
```



* This property is **static**.


***

### emptyArgumentList



```php
private static $emptyArgumentList
```



* This property is **static**.


***

### importPaths



```php
protected array&lt;int,string|callable&gt; $importPaths
```






***

### importCache



```php
protected array&lt;string,\ScssPhp\ScssPhp\Block&gt; $importCache
```






***

### importedFiles



```php
protected string[] $importedFiles
```






***

### userFunctions



```php
protected array $userFunctions
```






***

### registeredVars



```php
protected array&lt;string,mixed&gt; $registeredVars
```






***

### registeredFeatures



```php
protected array&lt;string,bool&gt; $registeredFeatures
```






***

### encoding



```php
protected string|null $encoding
```






***

### lineNumberStyle



```php
protected null $lineNumberStyle
```




* **Warning:** this property is **deprecated**. This means that this property will likely be removed in a future version.



***

### sourceMap



```php
protected int|\ScssPhp\ScssPhp\SourceMap\SourceMapGenerator $sourceMap
```






***

### sourceMapOptions



```php
protected array $sourceMapOptions
```






***

### charset



```php
private bool $charset
```






***

### formatter



```php
protected \ScssPhp\ScssPhp\Formatter $formatter
```






***

### configuredFormatter



```php
private string $configuredFormatter
```






***

### rootEnv



```php
protected \ScssPhp\ScssPhp\Compiler\Environment $rootEnv
```






***

### rootBlock



```php
protected \ScssPhp\ScssPhp\Formatter\OutputBlock|null $rootBlock
```






***

### env



```php
protected \ScssPhp\ScssPhp\Compiler\Environment $env
```






***

### scope



```php
protected \ScssPhp\ScssPhp\Formatter\OutputBlock|null $scope
```






***

### storeEnv



```php
protected \ScssPhp\ScssPhp\Compiler\Environment|null $storeEnv
```






***

### charsetSeen



```php
protected bool|null $charsetSeen
```




* **Warning:** this property is **deprecated**. This means that this property will likely be removed in a future version.



***

### sourceNames



```php
protected array&lt;int,string|null&gt; $sourceNames
```






***

### cache



```php
protected \ScssPhp\ScssPhp\Cache|null $cache
```






***

### cacheCheckImportResolutions



```php
protected bool $cacheCheckImportResolutions
```






***

### indentLevel



```php
protected int $indentLevel
```






***

### extends



```php
protected array[] $extends
```






***

### extendsMap



```php
protected array&lt;string,int[]&gt; $extendsMap
```






***

### parsedFiles



```php
protected array&lt;string,int&gt; $parsedFiles
```






***

### parser



```php
protected \ScssPhp\ScssPhp\Parser|null $parser
```






***

### sourceIndex



```php
protected int|null $sourceIndex
```






***

### sourceLine



```php
protected int|null $sourceLine
```






***

### sourceColumn



```php
protected int|null $sourceColumn
```






***

### shouldEvaluate



```php
protected bool|null $shouldEvaluate
```






***

### ignoreErrors



```php
protected null $ignoreErrors
```




* **Warning:** this property is **deprecated**. This means that this property will likely be removed in a future version.



***

### ignoreCallStackMessage



```php
protected bool $ignoreCallStackMessage
```






***

### callStack



```php
protected array[] $callStack
```






***

### resolvedImports



```php
private array $resolvedImports
```






***

### currentDirectory

The directory of the currently processed file

```php
private string|null $currentDirectory
```






***

### rootDirectory

The directory of the input file

```php
private string $rootDirectory
```






***

### legacyCwdImportPath



```php
private bool $legacyCwdImportPath
```






***

### logger



```php
private \ScssPhp\ScssPhp\Logger\LoggerInterface $logger
```






***

### warnedChildFunctions



```php
private array&lt;string,bool&gt; $warnedChildFunctions
```






***

### libCall



```php
protected static $libCall
```



* This property is **static**.


***

### libGetFunction



```php
protected static $libGetFunction
```



* This property is **static**.


***

### libIf



```php
protected static $libIf
```



* This property is **static**.


***

### libIndex



```php
protected static $libIndex
```



* This property is **static**.


***

### libRgb



```php
protected static $libRgb
```



* This property is **static**.


***

### libRgba



```php
protected static $libRgba
```



* This property is **static**.


***

### libAdjustColor



```php
protected static $libAdjustColor
```



* This property is **static**.


***

### libChangeColor



```php
protected static $libChangeColor
```



* This property is **static**.


***

### libScaleColor



```php
protected static $libScaleColor
```



* This property is **static**.


***

### libIeHexStr



```php
protected static $libIeHexStr
```



* This property is **static**.


***

### libRed



```php
protected static $libRed
```



* This property is **static**.


***

### libGreen



```php
protected static $libGreen
```



* This property is **static**.


***

### libBlue



```php
protected static $libBlue
```



* This property is **static**.


***

### libAlpha



```php
protected static $libAlpha
```



* This property is **static**.


***

### libOpacity



```php
protected static $libOpacity
```



* This property is **static**.


***

### libMix



```php
protected static $libMix
```



* This property is **static**.


***

### libHsl



```php
protected static $libHsl
```



* This property is **static**.


***

### libHsla



```php
protected static $libHsla
```



* This property is **static**.


***

### libHue



```php
protected static $libHue
```



* This property is **static**.


***

### libSaturation



```php
protected static $libSaturation
```



* This property is **static**.


***

### libLightness



```php
protected static $libLightness
```



* This property is **static**.


***

### libAdjustHue



```php
protected static $libAdjustHue
```



* This property is **static**.


***

### libLighten



```php
protected static $libLighten
```



* This property is **static**.


***

### libDarken



```php
protected static $libDarken
```



* This property is **static**.


***

### libSaturate



```php
protected static $libSaturate
```



* This property is **static**.


***

### libDesaturate



```php
protected static $libDesaturate
```



* This property is **static**.


***

### libGrayscale



```php
protected static $libGrayscale
```



* This property is **static**.


***

### libComplement



```php
protected static $libComplement
```



* This property is **static**.


***

### libInvert



```php
protected static $libInvert
```



* This property is **static**.


***

### libOpacify



```php
protected static $libOpacify
```



* This property is **static**.


***

### libFadeIn



```php
protected static $libFadeIn
```



* This property is **static**.


***

### libTransparentize



```php
protected static $libTransparentize
```



* This property is **static**.


***

### libFadeOut



```php
protected static $libFadeOut
```



* This property is **static**.


***

### libUnquote



```php
protected static $libUnquote
```



* This property is **static**.


***

### libQuote



```php
protected static $libQuote
```



* This property is **static**.


***

### libPercentage



```php
protected static $libPercentage
```



* This property is **static**.


***

### libRound



```php
protected static $libRound
```



* This property is **static**.


***

### libFloor



```php
protected static $libFloor
```



* This property is **static**.


***

### libCeil



```php
protected static $libCeil
```



* This property is **static**.


***

### libAbs



```php
protected static $libAbs
```



* This property is **static**.


***

### libMin



```php
protected static $libMin
```



* This property is **static**.


***

### libMax



```php
protected static $libMax
```



* This property is **static**.


***

### libLength



```php
protected static $libLength
```



* This property is **static**.


***

### libListSeparator



```php
protected static $libListSeparator
```



* This property is **static**.


***

### libNth



```php
protected static $libNth
```



* This property is **static**.


***

### libSetNth



```php
protected static $libSetNth
```



* This property is **static**.


***

### libMapGet



```php
protected static $libMapGet
```



* This property is **static**.


***

### libMapKeys



```php
protected static $libMapKeys
```



* This property is **static**.


***

### libMapValues



```php
protected static $libMapValues
```



* This property is **static**.


***

### libMapRemove



```php
protected static $libMapRemove
```



* This property is **static**.


***

### libMapHasKey



```php
protected static $libMapHasKey
```



* This property is **static**.


***

### libMapMerge



```php
protected static $libMapMerge
```



* This property is **static**.


***

### libKeywords



```php
protected static $libKeywords
```



* This property is **static**.


***

### libIsBracketed



```php
protected static $libIsBracketed
```



* This property is **static**.


***

### libJoin



```php
protected static $libJoin
```



* This property is **static**.


***

### libAppend



```php
protected static $libAppend
```



* This property is **static**.


***

### libZip



```php
protected static $libZip
```



* This property is **static**.


***

### libTypeOf



```php
protected static $libTypeOf
```



* This property is **static**.


***

### libUnit



```php
protected static $libUnit
```



* This property is **static**.


***

### libUnitless



```php
protected static $libUnitless
```



* This property is **static**.


***

### libComparable



```php
protected static $libComparable
```



* This property is **static**.


***

### libStrIndex



```php
protected static $libStrIndex
```



* This property is **static**.


***

### libStrInsert



```php
protected static $libStrInsert
```



* This property is **static**.


***

### libStrLength



```php
protected static $libStrLength
```



* This property is **static**.


***

### libStrSlice



```php
protected static $libStrSlice
```



* This property is **static**.


***

### libToLowerCase



```php
protected static $libToLowerCase
```



* This property is **static**.


***

### libToUpperCase



```php
protected static $libToUpperCase
```



* This property is **static**.


***

### libFeatureExists



```php
protected static $libFeatureExists
```



* This property is **static**.


***

### libFunctionExists



```php
protected static $libFunctionExists
```



* This property is **static**.


***

### libGlobalVariableExists



```php
protected static $libGlobalVariableExists
```



* This property is **static**.


***

### libMixinExists



```php
protected static $libMixinExists
```



* This property is **static**.


***

### libVariableExists



```php
protected static $libVariableExists
```



* This property is **static**.


***

### libCounter



```php
protected static $libCounter
```



* This property is **static**.


***

### libRandom



```php
protected static $libRandom
```



* This property is **static**.


***

### libUniqueId



```php
protected static $libUniqueId
```



* This property is **static**.


***

### libInspect



```php
protected static $libInspect
```



* This property is **static**.


***

### libIsSuperselector



```php
protected static $libIsSuperselector
```



* This property is **static**.


***

### libSelectorAppend



```php
protected static $libSelectorAppend
```



* This property is **static**.


***

### libSelectorExtend



```php
protected static $libSelectorExtend
```



* This property is **static**.


***

### libSelectorReplace



```php
protected static $libSelectorReplace
```



* This property is **static**.


***

### libSelectorNest



```php
protected static $libSelectorNest
```



* This property is **static**.


***

### libSelectorParse



```php
protected static $libSelectorParse
```



* This property is **static**.


***

### libSelectorUnify



```php
protected static $libSelectorUnify
```



* This property is **static**.


***

### libSimpleSelectors



```php
protected static $libSimpleSelectors
```



* This property is **static**.


***

### libScssphpGlob



```php
protected static $libScssphpGlob
```



* This property is **static**.


***

## Methods


### __construct

Constructor

```php
public __construct(array|null $cacheOptions = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cacheOptions` | **array&#124;null** |  |





***

### setLogger

Sets an alternative logger.

```php
public setLogger(\ScssPhp\ScssPhp\Logger\LoggerInterface $logger): void
```

Changing the logger in the middle of the compilation is not
supported and will result in an undefined behavior.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$logger` | **\ScssPhp\ScssPhp\Logger\LoggerInterface** |  |





***

### setErrorOuput

Set an alternative error output stream, for testing purpose only

```php
public setErrorOuput(resource $handle): void
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$handle` | **resource** |  |





***

### compile

Compile scss

```php
public compile(string $code, string|null $path = null): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$code` | **string** |  |
| `$path` | **string&#124;null** |  |




**Throws:**
<p>when the source fails to compile</p>

- [`SassException`](./Exception/SassException.md)



***

### compileFile

Compiles the provided scss file into CSS.

```php
public compileFile(string $path): \ScssPhp\ScssPhp\CompilationResult
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |




**Throws:**
<p>when the source fails to compile</p>

- [`SassException`](./Exception/SassException.md)



***

### compileString

Compiles the provided scss source code into CSS.

```php
public compileString(string $source, string|null $path = null): \ScssPhp\ScssPhp\CompilationResult
```

If provided, the path is considered to be the path from which the source code comes
from, which will be used to resolve relative imports.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **string** |  |
| `$path` | **string&#124;null** | The path for the source, used to resolve relative imports |




**Throws:**
<p>when the source fails to compile</p>

- [`SassException`](./Exception/SassException.md)



***

### isFreshCachedResult



```php
private isFreshCachedResult(\ScssPhp\ScssPhp\Compiler\CachedResult $result): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$result` | **\ScssPhp\ScssPhp\Compiler\CachedResult** |  |





***

### parserFactory

Instantiate parser

```php
protected parserFactory(string|null $path): \ScssPhp\ScssPhp\Parser
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string&#124;null** |  |





***

### isSelfExtend

Is self extend?

```php
protected isSelfExtend(array $target, array $origin): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$target` | **array** |  |
| `$origin` | **array** |  |





***

### pushExtends

Push extends

```php
protected pushExtends(string[] $target, array $origin, array|null $block): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$target` | **string[]** |  |
| `$origin` | **array** |  |
| `$block` | **array&#124;null** |  |





***

### makeOutputBlock

Make output block

```php
protected makeOutputBlock(string|null $type, string[]|null $selectors = null): \ScssPhp\ScssPhp\Formatter\OutputBlock
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **string&#124;null** |  |
| `$selectors` | **string[]&#124;null** |  |





***

### compileRoot

Compile root

```php
protected compileRoot(\ScssPhp\ScssPhp\Block $rootBlock): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rootBlock` | **\ScssPhp\ScssPhp\Block** |  |





***

### missingSelectors

Report missing selectors

```php
protected missingSelectors(): void
```












***

### flattenSelectors

Flatten selectors

```php
protected flattenSelectors(\ScssPhp\ScssPhp\Formatter\OutputBlock $block, string $parentKey = null): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$block` | **\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |
| `$parentKey` | **string** |  |





***

### glueFunctionSelectors

Glue parts of :not( or :nth-child( ... that are in general split in selectors parts

```php
protected glueFunctionSelectors(array $parts): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parts` | **array** |  |





***

### matchExtends

Match extends

```php
protected matchExtends(array $selector, array& $out, int $from, bool $initial = true): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$selector` | **array** |  |
| `$out` | **array** |  |
| `$from` | **int** |  |
| `$initial` | **bool** |  |





***

### isPseudoSelector

Test a part for being a pseudo selector

```php
protected isPseudoSelector(string $part, array& $matches): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$part` | **string** |  |
| `$matches` | **array** |  |





***

### pushOrMergeExtentedSelector

Push extended selector except if
 - this is a pseudo selector
 - same as previous
 - in a white list
in this case we merge the pseudo selector content

```php
protected pushOrMergeExtentedSelector(array& $out, array $extended): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$out` | **array** |  |
| `$extended` | **array** |  |





***

### matchExtendsSingle

Match extends single

```php
protected matchExtendsSingle(array $rawSingle, array& $outOrigin, bool $initial = true): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rawSingle` | **array** |  |
| `$outOrigin` | **array** |  |
| `$initial` | **bool** |  |





***

### extractRelationshipFromFragment

Extract a relationship from the fragment.

```php
protected extractRelationshipFromFragment(array $fragment): array
```

When extracting the last portion of a selector we will be left with a
fragment which may end with a direction relationship combinator. This
method will extract the relationship fragment and return it along side
the rest.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fragment` | **array** | The selector fragment maybe ending with a direction relationship combinator. |


**Return Value:**

The selector without the relationship fragment if any, the relationship fragment.




***

### combineSelectorSingle

Combine selector single

```php
protected combineSelectorSingle(array $base, array $other): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$base` | **array** |  |
| `$other` | **array** |  |





***

### compileMedia

Compile media

```php
protected compileMedia(\ScssPhp\ScssPhp\Block $media): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$media` | **\ScssPhp\ScssPhp\Block** |  |





***

### mediaParent

Media parent

```php
protected mediaParent(\ScssPhp\ScssPhp\Formatter\OutputBlock $scope): \ScssPhp\ScssPhp\Formatter\OutputBlock
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scope` | **\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |





***

### compileDirective

Compile directive

```php
protected compileDirective(\ScssPhp\ScssPhp\Block\DirectiveBlock|array $directive, \ScssPhp\ScssPhp\Formatter\OutputBlock $out): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$directive` | **\ScssPhp\ScssPhp\Block\DirectiveBlock&#124;array** |  |
| `$out` | **\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |





***

### compileDirectiveName

directive names can include some interpolation

```php
protected compileDirectiveName(string|array $directiveName): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$directiveName` | **string&#124;array** |  |




**Throws:**

- [`CompilerException`](./Exception/CompilerException.md)



***

### compileAtRoot

Compile at-root

```php
protected compileAtRoot(\ScssPhp\ScssPhp\Block $block): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$block` | **\ScssPhp\ScssPhp\Block** |  |





***

### filterScopeWithWithout

Filter at-root scope depending on with/without option

```php
protected filterScopeWithWithout(\ScssPhp\ScssPhp\Formatter\OutputBlock $scope, array $with, array $without): \ScssPhp\ScssPhp\Formatter\OutputBlock
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scope` | **\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |
| `$with` | **array** |  |
| `$without` | **array** |  |





***

### completeScope

found missing selector from a at-root compilation in the previous scope
(if at-root is just enclosing a property, the selector is in the parent tree)

```php
protected completeScope(\ScssPhp\ScssPhp\Formatter\OutputBlock $scope, \ScssPhp\ScssPhp\Formatter\OutputBlock $previousScope): \ScssPhp\ScssPhp\Formatter\OutputBlock
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scope` | **\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |
| `$previousScope` | **\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |





***

### findScopeSelectors

Find a selector by the depth node in the scope

```php
protected findScopeSelectors(\ScssPhp\ScssPhp\Formatter\OutputBlock $scope, int $depth): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scope` | **\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |
| `$depth` | **int** |  |





***

### compileWith

Compile @at-root's with: inclusion / without: exclusion into 2 lists uses to filter scope/env later

```php
protected compileWith(array|null $withCondition): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$withCondition` | **array&#124;null** |  |





***

### filterWithWithout

Filter env stack

```php
protected filterWithWithout(\ScssPhp\ScssPhp\Compiler\Environment[] $envs, array $with, array $without): \ScssPhp\ScssPhp\Compiler\Environment
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$envs` | **\ScssPhp\ScssPhp\Compiler\Environment[]** |  |
| `$with` | **array** |  |
| `$without` | **array** |  |





***

### isWith

Filter WITH rules

```php
protected isWith(\ScssPhp\ScssPhp\Block|\ScssPhp\ScssPhp\Formatter\OutputBlock $block, array $with, array $without): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$block` | **\ScssPhp\ScssPhp\Block&#124;\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |
| `$with` | **array** |  |
| `$without` | **array** |  |





***

### testWithWithout

Test a single type of block against with/without lists

```php
protected testWithWithout(string $what, array $with, array $without): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$what` | **string** |  |
| `$with` | **array** |  |
| `$without` | **array** |  |


**Return Value:**


true if the block should be kept, false to reject




***

### compileKeyframeBlock

Compile keyframe block

```php
protected compileKeyframeBlock(\ScssPhp\ScssPhp\Block $block, string[] $selectors): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$block` | **\ScssPhp\ScssPhp\Block** |  |
| `$selectors` | **string[]** |  |





***

### compileNestedPropertiesBlock

Compile nested properties lines

```php
protected compileNestedPropertiesBlock(\ScssPhp\ScssPhp\Block $block, \ScssPhp\ScssPhp\Formatter\OutputBlock $out): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$block` | **\ScssPhp\ScssPhp\Block** |  |
| `$out` | **\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |





***

### compileNestedBlock

Compile nested block

```php
protected compileNestedBlock(\ScssPhp\ScssPhp\Block $block, string[] $selectors): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$block` | **\ScssPhp\ScssPhp\Block** |  |
| `$selectors` | **string[]** |  |





***

### compileBlock

Recursively compiles a block.

```php
protected compileBlock(\ScssPhp\ScssPhp\Block $block): void
```

A block is analogous to a CSS block in most cases. A single SCSS document
is encapsulated in a block when parsed, but it does not have parent tags
so all of its children appear on the root level when compiled.

Blocks are made up of selectors and children.

The children of a block are just all the blocks that are defined within.

Compiling the block involves pushing a fresh environment on the stack,
and iterating through the props, compiling each one.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$block` | **\ScssPhp\ScssPhp\Block** |  |





**See Also:**

* \ScssPhp\ScssPhp\Compiler::compileChild() - 

***

### compileCommentValue

Compile the value of a comment that can have interpolation

```php
protected compileCommentValue(array $value, bool $pushEnv = false): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array** |  |
| `$pushEnv` | **bool** |  |





***

### compileComment

Compile root level comment

```php
protected compileComment(array $block): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$block` | **array** |  |





***

### evalSelectors

Evaluate selectors

```php
protected evalSelectors(array $selectors): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$selectors` | **array** |  |





***

### evalSelector

Evaluate selector

```php
protected evalSelector(array $selector): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$selector` | **array** |  |





***

### evalSelectorPart

Evaluate selector part; replaces all the interpolates, stripping quotes

```php
protected evalSelectorPart(array $part): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$part` | **array** |  |





***

### collapseSelectors

Collapse selectors

```php
protected collapseSelectors(array $selectors): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$selectors` | **array** |  |





***

### collapseSelectorsAsList

Collapse selectors

```php
private collapseSelectorsAsList(array $selectors): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$selectors` | **array** |  |





***

### replaceSelfSelector

Parse down the selector and revert [self] to "&" before a reparsing

```php
protected replaceSelfSelector(array $selectors, string|null $replace = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$selectors` | **array** |  |
| `$replace` | **string&#124;null** |  |





***

### flattenSelectorSingle

Flatten selector single; joins together .classes and #ids

```php
protected flattenSelectorSingle(array $single): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$single` | **array** |  |





***

### compileSelector

Compile selector to string; self(&) should have been replaced by now

```php
protected compileSelector(string|array $selector): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$selector` | **string&#124;array** |  |





***

### compileSelectorPart

Compile selector part

```php
protected compileSelectorPart(array $piece): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$piece` | **array** |  |





***

### hasSelectorPlaceholder

Has selector placeholder?

```php
protected hasSelectorPlaceholder(array $selector): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$selector` | **array** |  |





***

### pushCallStack



```php
protected pushCallStack(string $name = &#039;&#039;): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### popCallStack



```php
protected popCallStack(): void
```












***

### compileChildren

Compile children and return result

```php
protected compileChildren(array $stms, \ScssPhp\ScssPhp\Formatter\OutputBlock $out, string $traceName = &#039;&#039;): array|\ScssPhp\ScssPhp\Node\Number|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stms` | **array** |  |
| `$out` | **\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |
| `$traceName` | **string** |  |





***

### compileChildrenNoReturn

Compile children and throw exception if unexpected at-return

```php
protected compileChildrenNoReturn(array[] $stms, \ScssPhp\ScssPhp\Formatter\OutputBlock $out, \ScssPhp\ScssPhp\Block $selfParent = null, string $traceName = &#039;&#039;): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stms` | **array[]** |  |
| `$out` | **\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |
| `$selfParent` | **\ScssPhp\ScssPhp\Block** |  |
| `$traceName` | **string** |  |




**Throws:**

- [`Exception`](../../Exception.md)



***

### evaluateMediaQuery

evaluate media query : compile internal value keeping the structure unchanged

```php
protected evaluateMediaQuery(array $queryList): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$queryList` | **array** |  |





***

### compileMediaQuery

Compile media query

```php
protected compileMediaQuery(array $queryList): string[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$queryList` | **array** |  |





***

### mergeDirectRelationships

Merge direct relationships between selectors

```php
protected mergeDirectRelationships(array $selectors1, array $selectors2): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$selectors1` | **array** |  |
| `$selectors2` | **array** |  |





***

### mergeMediaTypes

Merge media types

```php
protected mergeMediaTypes(array $type1, array $type2): array|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type1` | **array** |  |
| `$type2` | **array** |  |





***

### compileImport

Compile import; returns true if the value was something that could be imported

```php
protected compileImport(array $rawPath, \ScssPhp\ScssPhp\Formatter\OutputBlock $out, bool $once = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rawPath` | **array** |  |
| `$out` | **\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |
| `$once` | **bool** |  |





***

### compileImportPath



```php
protected compileImportPath(array $rawPath): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rawPath` | **array** |  |




**Throws:**

- [`CompilerException`](./Exception/CompilerException.md)



***

### escapeImportPathString



```php
protected escapeImportPathString(array $path): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **array** |  |




**Throws:**

- [`CompilerException`](./Exception/CompilerException.md)



***

### appendRootDirective

Append a root directive like @import or @charset as near as the possible from the source code
(keeping before comments, @import and @charset coming before in the source code)

```php
protected appendRootDirective(string $line, \ScssPhp\ScssPhp\Formatter\OutputBlock $out, array $allowed = [Type::T_COMMENT]): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$line` | **string** |  |
| `$out` | **\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |
| `$allowed` | **array** |  |





***

### appendOutputLine

Append lines to the current output block:
directly to the block or through a child if necessary

```php
protected appendOutputLine(\ScssPhp\ScssPhp\Formatter\OutputBlock $out, string $type, string $line): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$out` | **\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |
| `$type` | **string** |  |
| `$line` | **string** |  |





***

### compileChild

Compile child; returns a value to halt execution

```php
protected compileChild(array $child, \ScssPhp\ScssPhp\Formatter\OutputBlock $out): array|\ScssPhp\ScssPhp\Node\Number|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$child` | **array** |  |
| `$out` | **\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |





***

### expToString

Reduce expression to string

```php
protected expToString(array $exp, bool $keepParens = false): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$exp` | **array** |  |
| `$keepParens` | **bool** |  |





***

### isTruthy

Is truthy?

```php
public isTruthy(array|\ScssPhp\ScssPhp\Node\Number $value): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |





***

### isImmediateRelationshipCombinator

Is the value a direct relationship combinator?

```php
protected isImmediateRelationshipCombinator(string $value): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **string** |  |





***

### shouldEval

Should $value cause its operand to eval

```php
protected shouldEval(array $value): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array** |  |





***

### reduce

Reduce value

```php
protected reduce(array|\ScssPhp\ScssPhp\Node\Number $value, bool $inExp = false): array|\ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$inExp` | **bool** |  |





***

### fncall

Function caller

```php
protected fncall(string|array $functionReference, array $argValues): array|\ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$functionReference` | **string&#124;array** |  |
| `$argValues` | **array** |  |





***

### cssValidArg



```php
protected cssValidArg(array|\ScssPhp\ScssPhp\Node\Number $arg, string[] $allowed_function = [], bool $inFunction = false): array|\ScssPhp\ScssPhp\Node\Number|false
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arg` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$allowed_function` | **string[]** |  |
| `$inFunction` | **bool** |  |





***

### stringifyFncallArgs

Reformat fncall arguments to proper css function output

```php
protected stringifyFncallArgs(array|\ScssPhp\ScssPhp\Node\Number $arg): array|\ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arg` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |





***

### getFunctionReference

Find a function reference

```php
protected getFunctionReference(string $name, bool $safeCopy = false): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$safeCopy` | **bool** |  |





***

### normalizeName

Normalize name

```php
protected normalizeName(string $name): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### opAddNumberNumber

Add numbers

```php
protected opAddNumberNumber(\ScssPhp\ScssPhp\Node\Number $left, \ScssPhp\ScssPhp\Node\Number $right): \ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### opMulNumberNumber

Multiply numbers

```php
protected opMulNumberNumber(\ScssPhp\ScssPhp\Node\Number $left, \ScssPhp\ScssPhp\Node\Number $right): \ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### opSubNumberNumber

Subtract numbers

```php
protected opSubNumberNumber(\ScssPhp\ScssPhp\Node\Number $left, \ScssPhp\ScssPhp\Node\Number $right): \ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### opDivNumberNumber

Divide numbers

```php
protected opDivNumberNumber(\ScssPhp\ScssPhp\Node\Number $left, \ScssPhp\ScssPhp\Node\Number $right): \ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### opModNumberNumber

Mod numbers

```php
protected opModNumberNumber(\ScssPhp\ScssPhp\Node\Number $left, \ScssPhp\ScssPhp\Node\Number $right): \ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### opAdd

Add strings

```php
protected opAdd(array $left, array $right): array|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **array** |  |
| `$right` | **array** |  |





***

### opAnd

Boolean and

```php
protected opAnd(array|\ScssPhp\ScssPhp\Node\Number $left, array|\ScssPhp\ScssPhp\Node\Number $right, bool $shouldEval): array|\ScssPhp\ScssPhp\Node\Number|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$shouldEval` | **bool** |  |





***

### opOr

Boolean or

```php
protected opOr(array|\ScssPhp\ScssPhp\Node\Number $left, array|\ScssPhp\ScssPhp\Node\Number $right, bool $shouldEval): array|\ScssPhp\ScssPhp\Node\Number|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$shouldEval` | **bool** |  |





***

### opColorColor

Compare colors

```php
protected opColorColor(string $op, array $left, array $right): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$op` | **string** |  |
| `$left` | **array** |  |
| `$right` | **array** |  |





***

### opColorNumber

Compare color and number

```php
protected opColorNumber(string $op, array $left, \ScssPhp\ScssPhp\Node\Number $right): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$op` | **string** |  |
| `$left` | **array** |  |
| `$right` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### opNumberColor

Compare number and color

```php
protected opNumberColor(string $op, \ScssPhp\ScssPhp\Node\Number $left, array $right): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$op` | **string** |  |
| `$left` | **\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **array** |  |





***

### opEq

Compare number1 == number2

```php
protected opEq(array|\ScssPhp\ScssPhp\Node\Number $left, array|\ScssPhp\ScssPhp\Node\Number $right): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |





***

### opNeq

Compare number1 != number2

```php
protected opNeq(array|\ScssPhp\ScssPhp\Node\Number $left, array|\ScssPhp\ScssPhp\Node\Number $right): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |





***

### opEqNumberNumber

Compare number1 == number2

```php
protected opEqNumberNumber(\ScssPhp\ScssPhp\Node\Number $left, \ScssPhp\ScssPhp\Node\Number $right): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### opNeqNumberNumber

Compare number1 != number2

```php
protected opNeqNumberNumber(\ScssPhp\ScssPhp\Node\Number $left, \ScssPhp\ScssPhp\Node\Number $right): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### opGteNumberNumber

Compare number1 >= number2

```php
protected opGteNumberNumber(\ScssPhp\ScssPhp\Node\Number $left, \ScssPhp\ScssPhp\Node\Number $right): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### opGtNumberNumber

Compare number1 > number2

```php
protected opGtNumberNumber(\ScssPhp\ScssPhp\Node\Number $left, \ScssPhp\ScssPhp\Node\Number $right): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### opLteNumberNumber

Compare number1 <= number2

```php
protected opLteNumberNumber(\ScssPhp\ScssPhp\Node\Number $left, \ScssPhp\ScssPhp\Node\Number $right): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### opLtNumberNumber

Compare number1 < number2

```php
protected opLtNumberNumber(\ScssPhp\ScssPhp\Node\Number $left, \ScssPhp\ScssPhp\Node\Number $right): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$left` | **\ScssPhp\ScssPhp\Node\Number** |  |
| `$right` | **\ScssPhp\ScssPhp\Node\Number** |  |





***

### toBool

Cast to boolean

```php
public toBool(bool $thing): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$thing` | **bool** |  |





***

### compileValue

Compiles a primitive value into a CSS property value.

```php
public compileValue(array|\ScssPhp\ScssPhp\Node\Number $value, bool $quote = true): string
```

Values in scssphp are typed by being wrapped in arrays, their format is
typically:

    array(type, contents [, additional_contents]*)

The input is expected to be reduced. This function will not work on
things like expressions and variables.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$quote` | **bool** |  |





***

### compileDebugValue



```php
protected compileDebugValue(array|\ScssPhp\ScssPhp\Node\Number $value): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |





***

### flattenList

Flatten list

```php
protected flattenList(array $list): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$list` | **array** |  |





***

### getStringText

Gets the text of a Sass string

```php
public getStringText(array $value): string
```

Calling this method on anything else than a SassString is unsupported. Use {@see \ScssPhp\ScssPhp\assertString} first
to ensure that the value is indeed a string.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array** |  |





***

### compileStringContent

Compile string content

```php
protected compileStringContent(array $string, bool $quote = true): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$string` | **array** |  |
| `$quote` | **bool** |  |





***

### extractInterpolation

Extract interpolation; it doesn't need to be recursive, compileValue will handle that

```php
protected extractInterpolation(array $list): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$list` | **array** |  |





***

### multiplySelectors

Find the final set of selectors

```php
protected multiplySelectors(\ScssPhp\ScssPhp\Compiler\Environment $env, \ScssPhp\ScssPhp\Block $selfParent = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$env` | **\ScssPhp\ScssPhp\Compiler\Environment** |  |
| `$selfParent` | **\ScssPhp\ScssPhp\Block** |  |





***

### joinSelectors

Join selectors; looks for & to replace, or append parent before child

```php
protected joinSelectors(array $parent, array $child, bool& $stillHasSelf, array $selfParentSelectors = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parent` | **array** |  |
| `$child` | **array** |  |
| `$stillHasSelf` | **bool** |  |
| `$selfParentSelectors` | **array** |  |





***

### multiplyMedia

Multiply media

```php
protected multiplyMedia(\ScssPhp\ScssPhp\Compiler\Environment $env = null, array $childQueries = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$env` | **\ScssPhp\ScssPhp\Compiler\Environment** |  |
| `$childQueries` | **array** |  |





***

### compactEnv

Convert env linked list to stack

```php
protected compactEnv(\ScssPhp\ScssPhp\Compiler\Environment $env): \ScssPhp\ScssPhp\Compiler\Environment[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$env` | **\ScssPhp\ScssPhp\Compiler\Environment** |  |





***

### extractEnv

Convert env stack to singly linked list

```php
protected extractEnv(\ScssPhp\ScssPhp\Compiler\Environment[] $envs): \ScssPhp\ScssPhp\Compiler\Environment
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$envs` | **\ScssPhp\ScssPhp\Compiler\Environment[]** |  |





***

### pushEnv

Push environment

```php
protected pushEnv(\ScssPhp\ScssPhp\Block $block = null): \ScssPhp\ScssPhp\Compiler\Environment
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$block` | **\ScssPhp\ScssPhp\Block** |  |





***

### popEnv

Pop environment

```php
protected popEnv(): void
```












***

### backPropagateEnv

Propagate vars from a just poped Env (used in @each and @for)

```php
protected backPropagateEnv(array $store, null|string[] $excludedVars = null): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$store` | **array** |  |
| `$excludedVars` | **null&#124;string[]** |  |





***

### getStoreEnv

Get store environment

```php
protected getStoreEnv(): \ScssPhp\ScssPhp\Compiler\Environment
```












***

### set

Set variable

```php
protected set(string $name, mixed $value, bool $shadow = false, \ScssPhp\ScssPhp\Compiler\Environment $env = null, mixed $valueUnreduced = null): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **mixed** |  |
| `$shadow` | **bool** |  |
| `$env` | **\ScssPhp\ScssPhp\Compiler\Environment** |  |
| `$valueUnreduced` | **mixed** |  |





***

### setExisting

Set existing variable

```php
protected setExisting(string $name, mixed $value, \ScssPhp\ScssPhp\Compiler\Environment $env, mixed $valueUnreduced = null): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **mixed** |  |
| `$env` | **\ScssPhp\ScssPhp\Compiler\Environment** |  |
| `$valueUnreduced` | **mixed** |  |





***

### setRaw

Set raw variable

```php
protected setRaw(string $name, mixed $value, \ScssPhp\ScssPhp\Compiler\Environment $env, mixed $valueUnreduced = null): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **mixed** |  |
| `$env` | **\ScssPhp\ScssPhp\Compiler\Environment** |  |
| `$valueUnreduced` | **mixed** |  |





***

### has

Has variable?

```php
protected has(string $name, \ScssPhp\ScssPhp\Compiler\Environment $env = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$env` | **\ScssPhp\ScssPhp\Compiler\Environment** |  |





***

### injectVariables

Inject variables

```php
protected injectVariables(array $args): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **array** |  |





***

### replaceVariables

Replaces variables.

```php
public replaceVariables(array&lt;string,mixed&gt; $variables): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$variables` | **array<string,mixed>** |  |





***

### addVariables

Replaces variables.

```php
public addVariables(array&lt;string,mixed&gt; $variables): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$variables` | **array<string,mixed>** |  |





***

### setVariables

Set variables

```php
public setVariables(array $variables): void
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$variables` | **array** |  |





***

### unsetVariable

Unset variable

```php
public unsetVariable(string $name): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### getVariables

Returns list of variables

```php
public getVariables(): array
```












***

### getParsedFiles

Returns list of parsed files

```php
public getParsedFiles(): array&lt;string,int&gt;
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### addImportPath

Add import path

```php
public addImportPath(string|callable $path): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string&#124;callable** |  |





***

### setImportPaths

Set import paths

```php
public setImportPaths(string|(string|callable)[] $path): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string&#124;(string&#124;callable)[]** |  |





***

### setNumberPrecision

Set number precision

```php
public setNumberPrecision(int $numberPrecision): void
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numberPrecision` | **int** |  |





***

### setOutputStyle

Sets the output style.

```php
public setOutputStyle(string $style): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$style` | **string** | One of the OutputStyle constants |





***

### setFormatter

Set formatter

```php
public setFormatter(string $formatterName): void
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$formatterName` | **string** |  |





***

### setLineNumberStyle

Set line number style

```php
public setLineNumberStyle(string $lineNumberStyle): void
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lineNumberStyle` | **string** |  |





***

### setCharset

Configures the handling of non-ASCII outputs.

```php
public setCharset(bool $charset): void
```

If $charset is `true`, this will include a `@charset` declaration or a
UTF-8 [byte-order mark][] if the stylesheet contains any non-ASCII
characters. Otherwise, it will never include a `@charset` declaration or a
byte-order mark.

[byte-order mark]: https://en.wikipedia.org/wiki/Byte_order_mark#UTF-8






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$charset` | **bool** |  |





***

### setSourceMap

Enable/disable source maps

```php
public setSourceMap(int $sourceMap): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sourceMap` | **int** |  |





***

### setSourceMapOptions

Set source map options

```php
public setSourceMapOptions(array $sourceMapOptions): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sourceMapOptions` | **array** |  |





***

### registerFunction

Register function

```php
public registerFunction(string $name, callable $callback, string[]|null $argumentDeclaration = null): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$callback` | **callable** |  |
| `$argumentDeclaration` | **string[]&#124;null** |  |





***

### reflectCallable



```php
private reflectCallable(callable $c): \ReflectionFunctionAbstract
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$c` | **callable** |  |





***

### unregisterFunction

Unregister function

```php
public unregisterFunction(string $name): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### addFeature

Add feature

```php
public addFeature(string $name): void
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |





***

### importFile

Import file

```php
protected importFile(string $path, \ScssPhp\ScssPhp\Formatter\OutputBlock $out): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |
| `$out` | **\ScssPhp\ScssPhp\Formatter\OutputBlock** |  |





***

### registerImport

Save the imported files with their resolving path context

```php
private registerImport(string|null $currentDirectory, string $path, string $filePath): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$currentDirectory` | **string&#124;null** |  |
| `$path` | **string** |  |
| `$filePath` | **string** |  |





***

### isCssImport

Detects whether the import is a CSS import.

```php
public static isCssImport(string $url): bool
```

For legacy reasons, custom importers are called for those, allowing them
to replace them with an actual Sass import. However this behavior is
deprecated. Custom importers are expected to return null when they receive
a CSS import.

* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** |  |





***

### resolveImportPath



```php
private resolveImportPath(string $url, string $baseDir): string|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$url` | **string** |  |
| `$baseDir` | **string** |  |





***

### checkImportPathConflicts



```php
private checkImportPathConflicts(string[] $paths): string|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$paths` | **string[]** |  |





***

### tryImportPathWithExtensions



```php
private tryImportPathWithExtensions(string $path): string[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### tryImportPath



```php
private tryImportPath(string $path): string[]
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### tryImportPathAsDirectory



```php
private tryImportPathAsDirectory(string $path): string|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string** |  |





***

### getPrettyPath



```php
private getPrettyPath(string|null $path): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$path` | **string&#124;null** |  |





***

### setEncoding

Set encoding

```php
public setEncoding(string|null $encoding): void
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$encoding` | **string&#124;null** |  |





***

### setIgnoreErrors

Ignore errors?

```php
public setIgnoreErrors(bool $ignoreErrors): \ScssPhp\ScssPhp\Compiler
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ignoreErrors` | **bool** |  |





***

### getSourcePosition

Get source position

```php
public getSourcePosition(): array
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.







***

### throwError

Throw error (exception)

```php
public throwError(string $msg): never
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$msg` | **string** | Message with optional sprintf()-style vararg parameters |




**Throws:**

- [`CompilerException`](./Exception/CompilerException.md)



***

### addLocationToMessage



```php
private addLocationToMessage(string $msg): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$msg` | **string** |  |





***

### errorArgsNumber



```php
public errorArgsNumber(string $functionName, array $ExpectedArgs, int $nbActual): \ScssPhp\ScssPhp\Exception\CompilerException
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$functionName` | **string** |  |
| `$ExpectedArgs` | **array** |  |
| `$nbActual` | **int** |  |





***

### callStackMessage

Beautify call stack for output

```php
protected callStackMessage(bool $all = false, int|null $limit = null): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$all` | **bool** |  |
| `$limit` | **int&#124;null** |  |





***

### handleImportLoop

Handle import loop

```php
protected handleImportLoop(string $name): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |




**Throws:**

- [`Exception`](../../Exception.md)



***

### callScssFunction

Call SCSS @function

```php
protected callScssFunction(\ScssPhp\ScssPhp\Block\CallableBlock|null $func, array $argValues): array|\ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$func` | **\ScssPhp\ScssPhp\Block\CallableBlock&#124;null** |  |
| `$argValues` | **array** |  |





***

### callNativeFunction

Call built-in and registered (PHP) functions

```php
protected callNativeFunction(string $name, callable $function, array $prototype, array $args): array|\ScssPhp\ScssPhp\Node\Number|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$function` | **callable** |  |
| `$prototype` | **array** |  |
| `$args` | **array** |  |





***

### getBuiltinFunction

Get built-in function

```php
protected getBuiltinFunction(string $name): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | Normalized name |





***

### sortNativeFunctionArgs

Sorts keyword arguments

```php
protected sortNativeFunctionArgs(string $functionName, array|null $prototypes, array $args): array|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$functionName` | **string** |  |
| `$prototypes` | **array&#124;null** |  |
| `$args` | **array** |  |





***

### parseFunctionPrototype

Parses a function prototype to the internal representation of arguments.

```php
private parseFunctionPrototype(string[] $prototype): array
```

The input is an array of strings describing each argument, as supported
in {@see \ScssPhp\ScssPhp\registerFunction}. Argument names don't include the `$`.
The output contains the list of positional argument, with their normalized
name (underscores are replaced by dashes), their original name (to be used
in case of error reporting) and their default value. The output also contains
the normalized name of the rest argument, or null if the function prototype
is not variadic.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prototype` | **string[]** |  |





***

### selectFunctionPrototype

Returns the function prototype for the given positional and named arguments.

```php
private selectFunctionPrototype(array[] $prototypes, int $positional, array&lt;string,string&gt; $names): array
```

If no exact match is found, finds the closest approximation. Note that this
doesn't guarantee that $positional and $names are valid for the returned
prototype.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prototypes` | **array[]** |  |
| `$positional` | **int** |  |
| `$names` | **array<string,string>** | A set of names, as both keys and values |





***

### checkPrototypeMatches

Checks whether the argument invocation matches the callable prototype.

```php
private checkPrototypeMatches(array $prototype, int $positional, array&lt;string,string&gt; $names): bool
```

The rules are similar to {@see \ScssPhp\ScssPhp\verifyPrototype}. The boolean return value
avoids the overhead of building and catching exceptions when the reason of
not matching the prototype does not need to be known.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prototype` | **array** |  |
| `$positional` | **int** |  |
| `$names` | **array<string,string>** |  |





***

### verifyPrototype

Verifies that the argument invocation is valid for the callable prototype.

```php
private verifyPrototype(array $prototype, int $positional, array&lt;string,string&gt; $names, bool $hasSplat): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prototype` | **array** |  |
| `$positional` | **int** |  |
| `$names` | **array<string,string>** |  |
| `$hasSplat` | **bool** |  |




**Throws:**

- [`SassScriptException`](./Exception/SassScriptException.md)



***

### evaluateArguments

Evaluates the argument from the invocation.

```php
private evaluateArguments(array[] $args, bool $reduce = true): array
```

This returns several things about this invocation:
- the list of positional arguments
- the map of named arguments, indexed by normalized names
- the set of names used in the arguments (that's an array using the normalized names as keys for O(1) access)
- the separator used by the list using the splat operator, if any
- a boolean indicator whether any splat argument (list or map) was used, to support the incomplete error reporting.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **array[]** |  |
| `$reduce` | **bool** | Whether arguments should be reduced to their value |




**Throws:**

- [`SassScriptException`](./Exception/SassScriptException.md)



***

### maybeReduce



```php
private maybeReduce(bool $reduce, array|\ScssPhp\ScssPhp\Node\Number $value): array|\ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reduce` | **bool** |  |
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |





***

### applyArguments

Apply argument values per definition

```php
protected applyArguments(array[] $argDef, array|null $argValues, bool $storeInEnv = true, bool $reduce = true): array&lt;string,array|\ScssPhp\ScssPhp\Node\Number&gt;
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$argDef` | **array[]** |  |
| `$argValues` | **array&#124;null** |  |
| `$storeInEnv` | **bool** |  |
| `$reduce` | **bool** | only used if $storeInEnv = false |




**Throws:**

- [`Exception`](../../Exception.md)



***

### applyArgumentsToDeclaration

Apply argument values per definition.

```php
private applyArgumentsToDeclaration(array $prototype, (array|\ScssPhp\ScssPhp\Node\Number)[] $positionalArgs, array&lt;string,array|\ScssPhp\ScssPhp\Node\Number&gt; $namedArgs, string|null $splatSeparator): array&lt;string,array|\ScssPhp\ScssPhp\Node\Number&gt;
```

This method assumes that the arguments are valid for the provided prototype.
The validation with {@see \ScssPhp\ScssPhp\verifyPrototype} must have been run before calling
it.
Arguments are returned as a map from the normalized argument names to the
value. Additional arguments are collected in a sass argument list available
under the name of the rest argument in the result.

Defaults are not applied as they are resolved in a different environment.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$prototype` | **array** |  |
| `$positionalArgs` | **(array&#124;\ScssPhp\ScssPhp\Node\Number)[]** |  |
| `$namedArgs` | **array<string,array&#124;\ScssPhp\ScssPhp\Node\Number>** |  |
| `$splatSeparator` | **string&#124;null** |  |





***

### coerceValue

Coerce a php value into a scss one

```php
protected coerceValue(mixed $value): array|\ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **mixed** |  |





***

### tryMap

Tries to convert an item to a Sass map

```php
private tryMap(\ScssPhp\ScssPhp\Node\Number|array $item): array|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **\ScssPhp\ScssPhp\Node\Number&#124;array** |  |





***

### coerceMap

Coerce something to map

```php
protected coerceMap(array|\ScssPhp\ScssPhp\Node\Number $item): array|\ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |





***

### coerceList

Coerce something to list

```php
protected coerceList(array|\ScssPhp\ScssPhp\Node\Number $item, string $delim = &#039;,&#039;, bool $removeTrailingNull = false): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$item` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$delim` | **string** |  |
| `$removeTrailingNull` | **bool** |  |





***

### coerceForExpression

Coerce color for expression

```php
protected coerceForExpression(array|\ScssPhp\ScssPhp\Node\Number $value): array|\ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |





***

### coerceColor

Coerce value to color

```php
protected coerceColor(array|\ScssPhp\ScssPhp\Node\Number $value, bool $inRGBFunction = false): array|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$inRGBFunction` | **bool** |  |





***

### compileRGBAValue



```php
protected compileRGBAValue(int|\ScssPhp\ScssPhp\Node\Number $value, bool $isAlpha = false): int|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **int&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$isAlpha` | **bool** |  |





***

### compileColorPartValue



```php
protected compileColorPartValue(mixed $value, int|float $min, int|float $max, bool $isInt = true): int|mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **mixed** |  |
| `$min` | **int&#124;float** |  |
| `$max` | **int&#124;float** |  |
| `$isInt` | **bool** |  |





***

### coerceString

Coerce value to string

```php
protected coerceString(array|\ScssPhp\ScssPhp\Node\Number $value): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |





***

### assertString

Assert value is a string

```php
public assertString(array|\ScssPhp\ScssPhp\Node\Number $value, string|null $varName = null): array
```

This method deals with internal implementation details of the value
representation where unquoted strings can sometimes be stored under
other types.
The returned value is always using the T_STRING type.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$varName` | **string&#124;null** |  |




**Throws:**

- [`SassScriptException`](./Exception/SassScriptException.md)



***

### coercePercent

Coerce value to a percentage

```php
protected coercePercent(array|\ScssPhp\ScssPhp\Node\Number $value): int|float
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |





***

### assertMap

Assert value is a map

```php
public assertMap(array|\ScssPhp\ScssPhp\Node\Number $value, string|null $varName = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$varName` | **string&#124;null** |  |




**Throws:**

- [`SassScriptException`](./Exception/SassScriptException.md)



***

### assertList

Assert value is a list

```php
public assertList(array|\ScssPhp\ScssPhp\Node\Number $value): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |




**Throws:**

- [`Exception`](../../Exception.md)



***

### getArgumentListKeywords

Gets the keywords of an argument list.

```php
public getArgumentListKeywords(array|\ScssPhp\ScssPhp\Node\Number $value): array&lt;string,array|\ScssPhp\ScssPhp\Node\Number&gt;
```

Keys in the returned array are normalized names (underscores are replaced with dashes)
without the leading `$`.
Calling this helper with anything that an argument list received for a rest argument
of the function argument declaration is not supported.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |





***

### assertColor

Assert value is a color

```php
public assertColor(array|\ScssPhp\ScssPhp\Node\Number $value, string|null $varName = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$varName` | **string&#124;null** |  |




**Throws:**

- [`SassScriptException`](./Exception/SassScriptException.md)



***

### assertNumber

Assert value is a number

```php
public assertNumber(array|\ScssPhp\ScssPhp\Node\Number $value, string|null $varName = null): \ScssPhp\ScssPhp\Node\Number
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$varName` | **string&#124;null** |  |




**Throws:**

- [`SassScriptException`](./Exception/SassScriptException.md)



***

### assertInteger

Assert value is a integer

```php
public assertInteger(array|\ScssPhp\ScssPhp\Node\Number $value, string|null $varName = null): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$varName` | **string&#124;null** |  |




**Throws:**

- [`SassScriptException`](./Exception/SassScriptException.md)



***

### extractSlashAlphaInColorFunction

Extract the  ... / alpha on the last argument of channel arg
in color functions

```php
private extractSlashAlphaInColorFunction(array $args): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **array** |  |





***

### fixColor

Make sure a color's components don't go out of bounds

```php
protected fixColor(array $c): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$c` | **array** |  |





***

### hueToRGB

Hue to RGB helper

```php
protected hueToRGB(float $m1, float $m2, float $h): float
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$m1` | **float** |  |
| `$m2` | **float** |  |
| `$h` | **float** |  |





***

### HWBtoRGB

Convert HWB to RGB
https://www.w3.org/TR/css-color-4/#hwb-to-rgb

```php
private HWBtoRGB(int|float $hue, int|float $whiteness, int|float $blackness): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$hue` | **int&#124;float** | H from 0 to 360 |
| `$whiteness` | **int&#124;float** | W from 0 to 100 |
| `$blackness` | **int&#124;float** | B from 0 to 100 |





***

### RGBtoHWB

Convert RGB to HWB

```php
private RGBtoHWB(int $red, int $green, int $blue): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$red` | **int** |  |
| `$green` | **int** |  |
| `$blue` | **int** |  |





***

### libCall



```php
protected libCall(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libGetFunction



```php
protected libGetFunction(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libIf



```php
protected libIf(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libIndex



```php
protected libIndex(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libRgb



```php
protected libRgb(array $args, array $kwargs, string $funcName = &#039;rgb&#039;): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **array** |  |
| `$kwargs` | **array** |  |
| `$funcName` | **string** |  |





***

### libRgba



```php
protected libRgba(mixed $args, mixed $kwargs): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |
| `$kwargs` | **mixed** |  |





***

### alterColor

Helper function for adjust_color, change_color, and scale_color

```php
protected alterColor((array|\ScssPhp\ScssPhp\Node\Number)[] $args, string $operation, callable $fn): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **(array&#124;\ScssPhp\ScssPhp\Node\Number)[]** |  |
| `$operation` | **string** |  |
| `$fn` | **callable** |  |





***

### libAdjustColor



```php
protected libAdjustColor(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libChangeColor



```php
protected libChangeColor(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libScaleColor



```php
protected libScaleColor(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libIeHexStr



```php
protected libIeHexStr(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libRed



```php
protected libRed(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libGreen



```php
protected libGreen(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libBlue



```php
protected libBlue(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libAlpha



```php
protected libAlpha(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libOpacity



```php
protected libOpacity(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libMix



```php
protected libMix(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libHsl



```php
protected libHsl(array $args, array $kwargs, string $funcName = &#039;hsl&#039;): array|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **array** |  |
| `$kwargs` | **array** |  |
| `$funcName` | **string** |  |





***

### libHsla



```php
protected libHsla(mixed $args, mixed $kwargs): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |
| `$kwargs` | **mixed** |  |





***

### libHue



```php
protected libHue(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libSaturation



```php
protected libSaturation(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libLightness



```php
protected libLightness(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### adjustHsl



```php
protected adjustHsl(array $color, int $idx, int|float $amount): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$color` | **array** |  |
| `$idx` | **int** |  |
| `$amount` | **int&#124;float** |  |





***

### libAdjustHue



```php
protected libAdjustHue(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libLighten



```php
protected libLighten(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libDarken



```php
protected libDarken(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libSaturate



```php
protected libSaturate(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libDesaturate



```php
protected libDesaturate(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libGrayscale



```php
protected libGrayscale(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libComplement



```php
protected libComplement(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libInvert



```php
protected libInvert(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libOpacify



```php
protected libOpacify(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libFadeIn



```php
protected libFadeIn(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libTransparentize



```php
protected libTransparentize(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libFadeOut



```php
protected libFadeOut(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libUnquote



```php
protected libUnquote(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libQuote



```php
protected libQuote(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libPercentage



```php
protected libPercentage(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libRound



```php
protected libRound(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libFloor



```php
protected libFloor(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libCeil



```php
protected libCeil(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libAbs



```php
protected libAbs(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libMin



```php
protected libMin(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libMax



```php
protected libMax(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libLength



```php
protected libLength(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libListSeparator



```php
protected libListSeparator(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libNth



```php
protected libNth(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libSetNth



```php
protected libSetNth(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libMapGet



```php
protected libMapGet(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### mapGet

Gets the value corresponding to that key in the map

```php
private mapGet(array $map, \ScssPhp\ScssPhp\Node\Number|array $key): \ScssPhp\ScssPhp\Node\Number|array|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$map` | **array** |  |
| `$key` | **\ScssPhp\ScssPhp\Node\Number&#124;array** |  |





***

### mapGetEntryIndex

Gets the index corresponding to that key in the map entries

```php
private mapGetEntryIndex(array $map, \ScssPhp\ScssPhp\Node\Number|array $key): int|null
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$map` | **array** |  |
| `$key` | **\ScssPhp\ScssPhp\Node\Number&#124;array** |  |





***

### libMapKeys



```php
protected libMapKeys(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libMapValues



```php
protected libMapValues(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libMapRemove



```php
protected libMapRemove(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libMapHasKey



```php
protected libMapHasKey(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### mapHasKey



```php
private mapHasKey(array $map, array|\ScssPhp\ScssPhp\Node\Number $keyValue): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$map` | **array** |  |
| `$keyValue` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |





***

### libMapMerge



```php
protected libMapMerge(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### modifyMap



```php
private modifyMap(array $map, array $keys, callable $modify, bool $addNesting = true): \ScssPhp\ScssPhp\Node\Number|array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$map` | **array** |  |
| `$keys` | **array** |  |
| `$modify` | **callable** |  |
| `$addNesting` | **bool** |  |





***

### modifyNestedMap



```php
private modifyNestedMap(array $map, array $keys, callable $modify, bool $addNesting): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$map` | **array** |  |
| `$keys` | **array** |  |
| `$modify` | **callable** |  |
| `$addNesting` | **bool** |  |





***

### mergeMaps

Merges 2 Sass maps together

```php
private mergeMaps(array $map1, array $map2): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$map1` | **array** |  |
| `$map2` | **array** |  |





***

### libKeywords



```php
protected libKeywords(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libIsBracketed



```php
protected libIsBracketed(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### listSeparatorForJoin



```php
protected listSeparatorForJoin(array $list1, array|\ScssPhp\ScssPhp\Node\Number|null $sep): string
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.



**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$list1` | **array** |  |
| `$sep` | **array&#124;\ScssPhp\ScssPhp\Node\Number&#124;null** |  |




**Throws:**

- [`CompilerException`](./Exception/CompilerException.md)



***

### libJoin



```php
protected libJoin(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libAppend



```php
protected libAppend(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libZip



```php
protected libZip(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libTypeOf



```php
protected libTypeOf(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### getTypeOf



```php
private getTypeOf(array|\ScssPhp\ScssPhp\Node\Number $value): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |





***

### libUnit



```php
protected libUnit(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libUnitless



```php
protected libUnitless(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libComparable



```php
protected libComparable(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libStrIndex



```php
protected libStrIndex(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libStrInsert



```php
protected libStrInsert(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libStrLength



```php
protected libStrLength(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libStrSlice



```php
protected libStrSlice(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libToLowerCase



```php
protected libToLowerCase(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libToUpperCase



```php
protected libToUpperCase(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### stringTransformAsciiOnly

Apply a filter on a string content, only on ascii chars
let extended chars untouched

```php
protected stringTransformAsciiOnly(string $stringContent, callable $filter): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stringContent` | **string** |  |
| `$filter` | **callable** |  |





***

### libFeatureExists



```php
protected libFeatureExists(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libFunctionExists



```php
protected libFunctionExists(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libGlobalVariableExists



```php
protected libGlobalVariableExists(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libMixinExists



```php
protected libMixinExists(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libVariableExists



```php
protected libVariableExists(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libCounter

Workaround IE7's content counter bug.

```php
protected libCounter(array $args): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **array** |  |





***

### libRandom



```php
protected libRandom(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libUniqueId



```php
protected libUniqueId(): mixed
```












***

### inspectFormatValue



```php
protected inspectFormatValue(array|\ScssPhp\ScssPhp\Node\Number $value, bool $force_enclosing_display = false): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$value` | **array&#124;\ScssPhp\ScssPhp\Node\Number** |  |
| `$force_enclosing_display` | **bool** |  |





***

### libInspect



```php
protected libInspect(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### getSelectorArg

Preprocess selector args

```php
protected getSelectorArg(array $arg, string|null $varname = null, bool $allowParent = false): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arg` | **array** |  |
| `$varname` | **string&#124;null** |  |
| `$allowParent` | **bool** |  |





***

### checkSelectorArgType

Check variable type for getSelectorArg() function

```php
protected checkSelectorArgType(array $arg, int $maxDepth = 2): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$arg` | **array** |  |
| `$maxDepth` | **int** |  |





***

### formatOutputSelector

Postprocess selector to output in right format

```php
protected formatOutputSelector(array $selectors): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$selectors` | **array** |  |





***

### libIsSuperselector



```php
protected libIsSuperselector(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### isSuperSelector

Test a $super selector again $sub

```php
protected isSuperSelector(array $super, array $sub): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$super` | **array** |  |
| `$sub` | **array** |  |





***

### isSuperPart

Test a part of super selector again a part of sub selector

```php
protected isSuperPart(array $superParts, array $subParts): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$superParts` | **array** |  |
| `$subParts` | **array** |  |





***

### libSelectorAppend



```php
protected libSelectorAppend(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### selectorAppend

Append parts of the last selector in the list to the previous, recursively

```php
protected selectorAppend(array $selectors): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$selectors` | **array** |  |




**Throws:**

- [`CompilerException`](./Exception/CompilerException.md)



***

### libSelectorExtend



```php
protected libSelectorExtend(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libSelectorReplace



```php
protected libSelectorReplace(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### extendOrReplaceSelectors

Extend/replace in selectors
used by selector-extend and selector-replace that use the same logic

```php
protected extendOrReplaceSelectors(array $selectors, array $extendee, array $extender, bool $replace = false): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$selectors` | **array** |  |
| `$extendee` | **array** |  |
| `$extender` | **array** |  |
| `$replace` | **bool** |  |





***

### libSelectorNest



```php
protected libSelectorNest(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libSelectorParse



```php
protected libSelectorParse(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libSelectorUnify



```php
protected libSelectorUnify(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### unifyCompoundSelectors

The selector-unify magic as its best
(at least works as expected on test cases)

```php
protected unifyCompoundSelectors(array $compound1, array $compound2): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compound1` | **array** |  |
| `$compound2` | **array** |  |





***

### prependSelectors

Prepend each selector from $selectors with $parts

```php
protected prependSelectors(array $selectors, array $parts): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$selectors` | **array** |  |
| `$parts` | **array** |  |





***

### matchPartInCompound

Try to find a matching part in a compound:
- with same html tag name
- with some class or id or something in common

```php
protected matchPartInCompound(array $part, array $compound): array|false
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$part` | **array** |  |
| `$compound` | **array** |  |





***

### mergeParts

Merge two part list taking care that
- the html tag is coming first - if any
- the :something are coming last

```php
protected mergeParts(array $parts1, array $parts2): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parts1` | **array** |  |
| `$parts2` | **array** |  |





***

### checkCompatibleTags

Check the compatibility between two tag names:
if both are defined they should be identical or one has to be '*'

```php
protected checkCompatibleTags(string $tag1, string $tag2): array|false
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tag1` | **string** |  |
| `$tag2` | **string** |  |





***

### findTagName

Find the html tag name in a selector parts list

```php
protected findTagName(string[] $parts): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$parts` | **string[]** |  |





***

### libSimpleSelectors



```php
protected libSimpleSelectors(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***

### libScssphpGlob



```php
protected libScssphpGlob(mixed $args): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$args` | **mixed** |  |





***


***
> Automatically generated on 2025-03-15
