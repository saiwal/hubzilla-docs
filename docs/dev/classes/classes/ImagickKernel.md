
# ImagickKernel





* Full name: `\ImagickKernel`

**See Also:**

* https://php.net/manual/en/class.imagickkernel.php - 




## Methods


### addKernel

Attach another kernel to this kernel to allow them to both be applied in a single morphology or filter function. Returns the new combined kernel.

```php
public addKernel(\ImagickKernel $imagickKernel): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$imagickKernel` | **\ImagickKernel** |  |





**See Also:**

* https://php.net/manual/en/imagickkernel.addkernel.php - 

***

### addUnityKernel

Adds a given amount of the 'Unity' Convolution Kernel to the given pre-scaled and normalized Kernel. This in effect adds that amount of the original image into the resulting convolution kernel. The resulting effect is to convert the defined kernels into blended soft-blurs, unsharp kernels or into sharpening kernels.

```php
public addUnityKernel(): void
```












**See Also:**

* https://php.net/manual/en/imagickkernel.addunitykernel.php - 

***

### fromBuiltin

Create a kernel from a builtin in kernel. See https://www.imagemagick.org/Usage/morphology/#kernel for examples.<br>
Currently the 'rotation' symbols are not supported. Example: $diamondKernel = ImagickKernel::fromBuiltIn(\Imagick::KERNEL_DIAMOND, "2");

```php
public static fromBuiltin(string $kernelType, string $kernelString): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$kernelType` | **string** | The type of kernel to build e.g. \Imagick::KERNEL_DIAMOND |
| `$kernelString` | **string** | A string that describes the parameters e.g. &quot;4,2.5&quot; |





**See Also:**

* https://php.net/manual/en/imagickkernel.frombuiltin.php - 

***

### fromMatrix

Create a kernel from a builtin in kernel. See https://www.imagemagick.org/Usage/morphology/#kernel for examples.<br>
Currently the 'rotation' symbols are not supported. Example: $diamondKernel = ImagickKernel::fromBuiltIn(\Imagick::KERNEL_DIAMOND, "2");

```php
public static fromMatrix(array $matrix, array $origin): \ImagickKernel
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matrix` | **array** | A matrix (i.e. 2d array) of values that define the kernel. Each element should be either a float value, or FALSE if that element shouldn&#039;t be used by the kernel. |
| `$origin` | **array** | [optional] Which element of the kernel should be used as the origin pixel. e.g. For a 3x3 matrix specifying the origin as [2, 2] would specify that the bottom right element should be the origin pixel. |





**See Also:**

* https://www.imagemagick.org/Usage/morphology/#kernel - * https://php.net/manual/en/imagickkernel.frombuiltin.php - 

***

### getMatrix

Get the 2d matrix of values used in this kernel. The elements are either float for elements that are used or 'false' if the element should be skipped.

```php
public getMatrix(): array
```









**Return Value:**

A matrix (2d array) of the values that represent the kernel.




**See Also:**

* https://php.net/manual/en/imagickkernel.getmatrix.php - 

***

### scale

ScaleKernelInfo() scales the given kernel list by the given amount, with or without normalization of the sum of the kernel values (as per given flags).<br>
The exact behaviour of this function depends on the normalization type being used please see https://www.imagemagick.org/api/morphology.php#ScaleKernelInfo for details.<br>
Flag should be one of Imagick::NORMALIZE_KERNEL_VALUE, Imagick::NORMALIZE_KERNEL_CORRELATE, Imagick::NORMALIZE_KERNEL_PERCENT or not set.

```php
public scale(): void
```












**See Also:**

* https://www.imagemagick.org/api/morphology.php#ScaleKernelInfo - * https://php.net/manual/en/imagickkernel.scale.php - 

***

### seperate

Separates a linked set of kernels and returns an array of ImagickKernels.

```php
public seperate(): void
```












**See Also:**

* https://php.net/manual/en/imagickkernel.separate.php - 

***


***
> Automatically generated on 2025-03-15
