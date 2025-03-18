
# miniApp

class miniApp

this is a transient structure which is needed to convert the $a->config settings
from older (existing) htconfig files which used a global App ($a) into the updated App structure
which is now static (although currently constructed at startup). We are only converting
'system' config settings.

* Full name: `\miniApp`



## Properties


### config



```php
public $config
```






***

## Methods


### convert



```php
public convert(): mixed
```












***


***
> Automatically generated on 2025-03-18
