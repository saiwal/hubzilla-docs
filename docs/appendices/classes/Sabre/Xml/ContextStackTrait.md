***

# ContextStackTrait

Context Stack.

The Context maintains information about a document during either reading or
writing.

During this process, it may be necessary to override this context
information.

This trait allows easy access to the context, and allows the end-user to
override its settings for document fragments, and easily restore it again
later.

* Full name: `\Sabre\Xml\ContextStackTrait`



## Properties


### elementMap

This is the element map. It contains a list of XML elements (in clark
notation) as keys and PHP class names as values.

```php
public array $elementMap
```

The PHP class names must implement Sabre\Xml\Element.

Values may also be a callable. In that case the function will be called
directly.




***

### contextUri

A contextUri pointing to the document being parsed / written.

```php
public string|null $contextUri
```

This uri may be used to resolve relative urls that may appear in the
document.

The reader and writer don't use this property, but as it's an extremely
common use-case for parsing XML documents, it's added here as a
convenience.




***

### namespaceMap

This is a list of namespaces that you want to give default prefixes.

```php
public array $namespaceMap
```

You must make sure you create this entire list before starting to write.
They should be registered on the root element.




***

### classMap

This is a list of custom serializers for specific classes.

```php
public array $classMap
```

The writer may use this if you attempt to serialize an object with a
class that does not implement XmlSerializable.

Instead it will look at this classmap to see if there is a custom
serializer here. This is useful if you don't want your value objects
to be responsible for serializing themselves.

The keys in this classmap need to be fully qualified PHP class names,
the values must be callbacks. The callbacks take two arguments. The
writer class, and the value that must be written.

function (Writer $writer, object $value)




***

### contextStack

Backups of previous contexts.

```php
protected array $contextStack
```






***

## Methods


### pushContext

Create a new "context".

```php
public pushContext(): mixed
```

This allows you to safely modify the elementMap, contextUri or
namespaceMap. After you're done, you can restore the old data again
with popContext.










***

### popContext

Restore the previous "context".

```php
public popContext(): mixed
```












***

***
> Automatically generated on 2025-03-18

