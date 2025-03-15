***

# QROutputInterface

Converts the data matrix into readable output



* Full name: `\chillerlan\QRCode\Output\QROutputInterface`


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`DEFAULT_MODULE_VALUES`|public| |[
    // light
    \chillerlan\QRCode\Data\QRMatrix::M_NULL =&gt; false,
    // 0
    \chillerlan\QRCode\Data\QRMatrix::M_DATA =&gt; false,
    // 4
    \chillerlan\QRCode\Data\QRMatrix::M_FINDER =&gt; false,
    // 6
    \chillerlan\QRCode\Data\QRMatrix::M_SEPARATOR =&gt; false,
    // 8
    \chillerlan\QRCode\Data\QRMatrix::M_ALIGNMENT =&gt; false,
    // 10
    \chillerlan\QRCode\Data\QRMatrix::M_TIMING =&gt; false,
    // 12
    \chillerlan\QRCode\Data\QRMatrix::M_FORMAT =&gt; false,
    // 14
    \chillerlan\QRCode\Data\QRMatrix::M_VERSION =&gt; false,
    // 16
    \chillerlan\QRCode\Data\QRMatrix::M_QUIETZONE =&gt; false,
    // 18
    \chillerlan\QRCode\Data\QRMatrix::M_LOGO =&gt; false,
    // 20
    \chillerlan\QRCode\Data\QRMatrix::M_TEST =&gt; false,
    // 255
    // dark
    \chillerlan\QRCode\Data\QRMatrix::M_DARKMODULE &lt;&lt; 8 =&gt; true,
    // 512
    \chillerlan\QRCode\Data\QRMatrix::M_DATA &lt;&lt; 8 =&gt; true,
    // 1024
    \chillerlan\QRCode\Data\QRMatrix::M_FINDER &lt;&lt; 8 =&gt; true,
    // 1536
    \chillerlan\QRCode\Data\QRMatrix::M_ALIGNMENT &lt;&lt; 8 =&gt; true,
    // 2560
    \chillerlan\QRCode\Data\QRMatrix::M_TIMING &lt;&lt; 8 =&gt; true,
    // 3072
    \chillerlan\QRCode\Data\QRMatrix::M_FORMAT &lt;&lt; 8 =&gt; true,
    // 3584
    \chillerlan\QRCode\Data\QRMatrix::M_VERSION &lt;&lt; 8 =&gt; true,
    // 4096
    \chillerlan\QRCode\Data\QRMatrix::M_FINDER_DOT &lt;&lt; 8 =&gt; true,
    // 5632
    \chillerlan\QRCode\Data\QRMatrix::M_TEST &lt;&lt; 8 =&gt; true,
]|

## Methods


### dump

generates the output, optionally dumps it to a file, and returns it

```php
public dump(string $file = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$file` | **string** |  |





***


***
> Automatically generated on 2025-03-15
