***

# HttpException

An exception representing a HTTP error.

This can be used as a generic exception in your application, if you'd like
to map HTTP errors to exceptions.

If you'd like to use this, create a new exception class, extending Exception
and implementing this interface.

* Full name: `\Sabre\HTTP\HttpException`



## Methods


### getHttpStatus

The http status code for the error.

```php
public getHttpStatus(): string|null
```

This may either be just the number, or a number and a human-readable
message, separated by a space.










***


***
> Automatically generated on 2025-03-15
