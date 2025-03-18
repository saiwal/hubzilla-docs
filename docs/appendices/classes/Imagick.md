
# Imagick





* Full name: `\Imagick`
* This class implements:
[`\Iterator`](./Iterator.md), [`\Countable`](./Countable.md)

**See Also:**

* https://php.net/manual/en/class.imagick.php - 


## Constants

| Constant | Visibility | Type | Value |
|:---------|:-----------|:-----|:------|
|`COLOR_BLACK`|public| |11|
|`COLOR_BLUE`|public| |12|
|`COLOR_CYAN`|public| |13|
|`COLOR_GREEN`|public| |14|
|`COLOR_RED`|public| |15|
|`COLOR_YELLOW`|public| |16|
|`COLOR_MAGENTA`|public| |17|
|`COLOR_OPACITY`|public| |18|
|`COLOR_ALPHA`|public| |19|
|`COLOR_FUZZ`|public| |20|
|`IMAGICK_EXTNUM`|public| |30403|
|`IMAGICK_EXTVER`|public| |&quot;3.4.3&quot;|
|`QUANTUM_RANGE`|public| |65535|
|`USE_ZEND_MM`|public| |0|
|`COMPOSITE_DEFAULT`|public| |40|
|`COMPOSITE_UNDEFINED`|public| |0|
|`COMPOSITE_NO`|public| |1|
|`COMPOSITE_ADD`|public| |2|
|`COMPOSITE_ATOP`|public| |3|
|`COMPOSITE_BLEND`|public| |4|
|`COMPOSITE_BUMPMAP`|public| |5|
|`COMPOSITE_CLEAR`|public| |7|
|`COMPOSITE_COLORBURN`|public| |8|
|`COMPOSITE_COLORDODGE`|public| |9|
|`COMPOSITE_COLORIZE`|public| |10|
|`COMPOSITE_COPYBLACK`|public| |11|
|`COMPOSITE_COPYBLUE`|public| |12|
|`COMPOSITE_COPY`|public| |13|
|`COMPOSITE_COPYCYAN`|public| |14|
|`COMPOSITE_COPYGREEN`|public| |15|
|`COMPOSITE_COPYMAGENTA`|public| |16|
|`COMPOSITE_COPYOPACITY`|public| |17|
|`COMPOSITE_COPYRED`|public| |18|
|`COMPOSITE_COPYYELLOW`|public| |19|
|`COMPOSITE_DARKEN`|public| |20|
|`COMPOSITE_DSTATOP`|public| |21|
|`COMPOSITE_DST`|public| |22|
|`COMPOSITE_DSTIN`|public| |23|
|`COMPOSITE_DSTOUT`|public| |24|
|`COMPOSITE_DSTOVER`|public| |25|
|`COMPOSITE_DIFFERENCE`|public| |26|
|`COMPOSITE_DISPLACE`|public| |27|
|`COMPOSITE_DISSOLVE`|public| |28|
|`COMPOSITE_EXCLUSION`|public| |29|
|`COMPOSITE_HARDLIGHT`|public| |30|
|`COMPOSITE_HUE`|public| |31|
|`COMPOSITE_IN`|public| |32|
|`COMPOSITE_LIGHTEN`|public| |33|
|`COMPOSITE_LUMINIZE`|public| |35|
|`COMPOSITE_MINUS`|public| |36|
|`COMPOSITE_MODULATE`|public| |37|
|`COMPOSITE_MULTIPLY`|public| |38|
|`COMPOSITE_OUT`|public| |39|
|`COMPOSITE_OVER`|public| |40|
|`COMPOSITE_OVERLAY`|public| |41|
|`COMPOSITE_PLUS`|public| |42|
|`COMPOSITE_REPLACE`|public| |43|
|`COMPOSITE_SATURATE`|public| |44|
|`COMPOSITE_SCREEN`|public| |45|
|`COMPOSITE_SOFTLIGHT`|public| |46|
|`COMPOSITE_SRCATOP`|public| |47|
|`COMPOSITE_SRC`|public| |48|
|`COMPOSITE_SRCIN`|public| |49|
|`COMPOSITE_SRCOUT`|public| |50|
|`COMPOSITE_SRCOVER`|public| |51|
|`COMPOSITE_SUBTRACT`|public| |52|
|`COMPOSITE_THRESHOLD`|public| |53|
|`COMPOSITE_XOR`|public| |54|
|`COMPOSITE_CHANGEMASK`|public| |6|
|`COMPOSITE_LINEARLIGHT`|public| |34|
|`COMPOSITE_DIVIDE`|public| |55|
|`COMPOSITE_DISTORT`|public| |56|
|`COMPOSITE_BLUR`|public| |57|
|`COMPOSITE_PEGTOPLIGHT`|public| |58|
|`COMPOSITE_VIVIDLIGHT`|public| |59|
|`COMPOSITE_PINLIGHT`|public| |60|
|`COMPOSITE_LINEARDODGE`|public| |61|
|`COMPOSITE_LINEARBURN`|public| |62|
|`COMPOSITE_MATHEMATICS`|public| |63|
|`COMPOSITE_MODULUSADD`|public| |2|
|`COMPOSITE_MODULUSSUBTRACT`|public| |52|
|`COMPOSITE_MINUSDST`|public| |36|
|`COMPOSITE_DIVIDEDST`|public| |55|
|`COMPOSITE_DIVIDESRC`|public| |64|
|`COMPOSITE_MINUSSRC`|public| |65|
|`COMPOSITE_DARKENINTENSITY`|public| |66|
|`COMPOSITE_LIGHTENINTENSITY`|public| |67|
|`MONTAGEMODE_FRAME`|public| |1|
|`MONTAGEMODE_UNFRAME`|public| |2|
|`MONTAGEMODE_CONCATENATE`|public| |3|
|`STYLE_NORMAL`|public| |1|
|`STYLE_ITALIC`|public| |2|
|`STYLE_OBLIQUE`|public| |3|
|`STYLE_ANY`|public| |4|
|`FILTER_UNDEFINED`|public| |0|
|`FILTER_POINT`|public| |1|
|`FILTER_BOX`|public| |2|
|`FILTER_TRIANGLE`|public| |3|
|`FILTER_HERMITE`|public| |4|
|`FILTER_HANNING`|public| |5|
|`FILTER_HAMMING`|public| |6|
|`FILTER_BLACKMAN`|public| |7|
|`FILTER_GAUSSIAN`|public| |8|
|`FILTER_QUADRATIC`|public| |9|
|`FILTER_CUBIC`|public| |10|
|`FILTER_CATROM`|public| |11|
|`FILTER_MITCHELL`|public| |12|
|`FILTER_LANCZOS`|public| |22|
|`FILTER_BESSEL`|public| |13|
|`FILTER_SINC`|public| |14|
|`FILTER_KAISER`|public| |16|
|`FILTER_WELSH`|public| |17|
|`FILTER_PARZEN`|public| |18|
|`FILTER_LAGRANGE`|public| |21|
|`FILTER_SENTINEL`|public| |31|
|`FILTER_BOHMAN`|public| |19|
|`FILTER_BARTLETT`|public| |20|
|`FILTER_JINC`|public| |13|
|`FILTER_SINCFAST`|public| |15|
|`FILTER_ROBIDOUX`|public| |26|
|`FILTER_LANCZOSSHARP`|public| |23|
|`FILTER_LANCZOS2`|public| |24|
|`FILTER_LANCZOS2SHARP`|public| |25|
|`FILTER_ROBIDOUXSHARP`|public| |27|
|`FILTER_COSINE`|public| |28|
|`FILTER_SPLINE`|public| |29|
|`FILTER_LANCZOSRADIUS`|public| |30|
|`IMGTYPE_UNDEFINED`|public| |0|
|`IMGTYPE_BILEVEL`|public| |1|
|`IMGTYPE_GRAYSCALE`|public| |2|
|`IMGTYPE_GRAYSCALEMATTE`|public| |3|
|`IMGTYPE_PALETTE`|public| |4|
|`IMGTYPE_PALETTEMATTE`|public| |5|
|`IMGTYPE_TRUECOLOR`|public| |6|
|`IMGTYPE_TRUECOLORMATTE`|public| |7|
|`IMGTYPE_COLORSEPARATION`|public| |8|
|`IMGTYPE_COLORSEPARATIONMATTE`|public| |9|
|`IMGTYPE_OPTIMIZE`|public| |10|
|`IMGTYPE_PALETTEBILEVELMATTE`|public| |11|
|`RESOLUTION_UNDEFINED`|public| |0|
|`RESOLUTION_PIXELSPERINCH`|public| |1|
|`RESOLUTION_PIXELSPERCENTIMETER`|public| |2|
|`COMPRESSION_UNDEFINED`|public| |0|
|`COMPRESSION_NO`|public| |1|
|`COMPRESSION_BZIP`|public| |2|
|`COMPRESSION_FAX`|public| |6|
|`COMPRESSION_GROUP4`|public| |7|
|`COMPRESSION_JPEG`|public| |8|
|`COMPRESSION_JPEG2000`|public| |9|
|`COMPRESSION_LOSSLESSJPEG`|public| |10|
|`COMPRESSION_LZW`|public| |11|
|`COMPRESSION_RLE`|public| |12|
|`COMPRESSION_ZIP`|public| |13|
|`COMPRESSION_DXT1`|public| |3|
|`COMPRESSION_DXT3`|public| |4|
|`COMPRESSION_DXT5`|public| |5|
|`COMPRESSION_ZIPS`|public| |14|
|`COMPRESSION_PIZ`|public| |15|
|`COMPRESSION_PXR24`|public| |16|
|`COMPRESSION_B44`|public| |17|
|`COMPRESSION_B44A`|public| |18|
|`COMPRESSION_LZMA`|public| |19|
|`COMPRESSION_JBIG1`|public| |20|
|`COMPRESSION_JBIG2`|public| |21|
|`PAINT_POINT`|public| |1|
|`PAINT_REPLACE`|public| |2|
|`PAINT_FLOODFILL`|public| |3|
|`PAINT_FILLTOBORDER`|public| |4|
|`PAINT_RESET`|public| |5|
|`GRAVITY_NORTHWEST`|public| |1|
|`GRAVITY_NORTH`|public| |2|
|`GRAVITY_NORTHEAST`|public| |3|
|`GRAVITY_WEST`|public| |4|
|`GRAVITY_CENTER`|public| |5|
|`GRAVITY_EAST`|public| |6|
|`GRAVITY_SOUTHWEST`|public| |7|
|`GRAVITY_SOUTH`|public| |8|
|`GRAVITY_SOUTHEAST`|public| |9|
|`GRAVITY_FORGET`|public| |0|
|`GRAVITY_STATIC`|public| |10|
|`STRETCH_NORMAL`|public| |1|
|`STRETCH_ULTRACONDENSED`|public| |2|
|`STRETCH_EXTRACONDENSED`|public| |3|
|`STRETCH_CONDENSED`|public| |4|
|`STRETCH_SEMICONDENSED`|public| |5|
|`STRETCH_SEMIEXPANDED`|public| |6|
|`STRETCH_EXPANDED`|public| |7|
|`STRETCH_EXTRAEXPANDED`|public| |8|
|`STRETCH_ULTRAEXPANDED`|public| |9|
|`STRETCH_ANY`|public| |10|
|`ALIGN_UNDEFINED`|public| |0|
|`ALIGN_LEFT`|public| |1|
|`ALIGN_CENTER`|public| |2|
|`ALIGN_RIGHT`|public| |3|
|`DECORATION_NO`|public| |1|
|`DECORATION_UNDERLINE`|public| |2|
|`DECORATION_OVERLINE`|public| |3|
|`DECORATION_LINETROUGH`|public| |4|
|`DECORATION_LINETHROUGH`|public| |4|
|`NOISE_UNIFORM`|public| |1|
|`NOISE_GAUSSIAN`|public| |2|
|`NOISE_MULTIPLICATIVEGAUSSIAN`|public| |3|
|`NOISE_IMPULSE`|public| |4|
|`NOISE_LAPLACIAN`|public| |5|
|`NOISE_POISSON`|public| |6|
|`NOISE_RANDOM`|public| |7|
|`CHANNEL_UNDEFINED`|public| |0|
|`CHANNEL_RED`|public| |1|
|`CHANNEL_GRAY`|public| |1|
|`CHANNEL_CYAN`|public| |1|
|`CHANNEL_GREEN`|public| |2|
|`CHANNEL_MAGENTA`|public| |2|
|`CHANNEL_BLUE`|public| |4|
|`CHANNEL_YELLOW`|public| |4|
|`CHANNEL_ALPHA`|public| |8|
|`CHANNEL_OPACITY`|public| |8|
|`CHANNEL_MATTE`|public| |8|
|`CHANNEL_BLACK`|public| |32|
|`CHANNEL_INDEX`|public| |32|
|`CHANNEL_ALL`|public| |134217727|
|`CHANNEL_DEFAULT`|public| |134217719|
|`CHANNEL_RGBA`|public| |15|
|`CHANNEL_TRUEALPHA`|public| |64|
|`CHANNEL_RGBS`|public| |128|
|`CHANNEL_GRAY_CHANNELS`|public| |128|
|`CHANNEL_SYNC`|public| |256|
|`CHANNEL_COMPOSITES`|public| |47|
|`METRIC_UNDEFINED`|public| |0|
|`METRIC_ABSOLUTEERRORMETRIC`|public| |1|
|`METRIC_MEANABSOLUTEERROR`|public| |2|
|`METRIC_MEANERRORPERPIXELMETRIC`|public| |3|
|`METRIC_MEANSQUAREERROR`|public| |4|
|`METRIC_PEAKABSOLUTEERROR`|public| |5|
|`METRIC_PEAKSIGNALTONOISERATIO`|public| |6|
|`METRIC_ROOTMEANSQUAREDERROR`|public| |7|
|`METRIC_NORMALIZEDCROSSCORRELATIONERRORMETRIC`|public| |8|
|`METRIC_FUZZERROR`|public| |9|
|`PIXEL_CHAR`|public| |1|
|`PIXEL_DOUBLE`|public| |2|
|`PIXEL_FLOAT`|public| |3|
|`PIXEL_INTEGER`|public| |4|
|`PIXEL_LONG`|public| |5|
|`PIXEL_QUANTUM`|public| |6|
|`PIXEL_SHORT`|public| |7|
|`EVALUATE_UNDEFINED`|public| |0|
|`EVALUATE_ADD`|public| |1|
|`EVALUATE_AND`|public| |2|
|`EVALUATE_DIVIDE`|public| |3|
|`EVALUATE_LEFTSHIFT`|public| |4|
|`EVALUATE_MAX`|public| |5|
|`EVALUATE_MIN`|public| |6|
|`EVALUATE_MULTIPLY`|public| |7|
|`EVALUATE_OR`|public| |8|
|`EVALUATE_RIGHTSHIFT`|public| |9|
|`EVALUATE_SET`|public| |10|
|`EVALUATE_SUBTRACT`|public| |11|
|`EVALUATE_XOR`|public| |12|
|`EVALUATE_POW`|public| |13|
|`EVALUATE_LOG`|public| |14|
|`EVALUATE_THRESHOLD`|public| |15|
|`EVALUATE_THRESHOLDBLACK`|public| |16|
|`EVALUATE_THRESHOLDWHITE`|public| |17|
|`EVALUATE_GAUSSIANNOISE`|public| |18|
|`EVALUATE_IMPULSENOISE`|public| |19|
|`EVALUATE_LAPLACIANNOISE`|public| |20|
|`EVALUATE_MULTIPLICATIVENOISE`|public| |21|
|`EVALUATE_POISSONNOISE`|public| |22|
|`EVALUATE_UNIFORMNOISE`|public| |23|
|`EVALUATE_COSINE`|public| |24|
|`EVALUATE_SINE`|public| |25|
|`EVALUATE_ADDMODULUS`|public| |26|
|`EVALUATE_MEAN`|public| |27|
|`EVALUATE_ABS`|public| |28|
|`EVALUATE_EXPONENTIAL`|public| |29|
|`EVALUATE_MEDIAN`|public| |30|
|`EVALUATE_SUM`|public| |31|
|`COLORSPACE_UNDEFINED`|public| |0|
|`COLORSPACE_RGB`|public| |1|
|`COLORSPACE_GRAY`|public| |2|
|`COLORSPACE_TRANSPARENT`|public| |3|
|`COLORSPACE_OHTA`|public| |4|
|`COLORSPACE_LAB`|public| |5|
|`COLORSPACE_XYZ`|public| |6|
|`COLORSPACE_YCBCR`|public| |7|
|`COLORSPACE_YCC`|public| |8|
|`COLORSPACE_YIQ`|public| |9|
|`COLORSPACE_YPBPR`|public| |10|
|`COLORSPACE_YUV`|public| |11|
|`COLORSPACE_CMYK`|public| |12|
|`COLORSPACE_SRGB`|public| |13|
|`COLORSPACE_HSB`|public| |14|
|`COLORSPACE_HSL`|public| |15|
|`COLORSPACE_HWB`|public| |16|
|`COLORSPACE_REC601LUMA`|public| |17|
|`COLORSPACE_REC709LUMA`|public| |19|
|`COLORSPACE_LOG`|public| |21|
|`COLORSPACE_CMY`|public| |22|
|`COLORSPACE_LUV`|public| |23|
|`COLORSPACE_HCL`|public| |24|
|`COLORSPACE_LCH`|public| |25|
|`COLORSPACE_LMS`|public| |26|
|`COLORSPACE_LCHAB`|public| |27|
|`COLORSPACE_LCHUV`|public| |28|
|`COLORSPACE_SCRGB`|public| |29|
|`COLORSPACE_HSI`|public| |30|
|`COLORSPACE_HSV`|public| |31|
|`COLORSPACE_HCLP`|public| |32|
|`COLORSPACE_YDBDR`|public| |33|
|`COLORSPACE_REC601YCBCR`|public| |18|
|`COLORSPACE_REC709YCBCR`|public| |20|
|`VIRTUALPIXELMETHOD_UNDEFINED`|public| |0|
|`VIRTUALPIXELMETHOD_BACKGROUND`|public| |1|
|`VIRTUALPIXELMETHOD_CONSTANT`|public| |2|
|`VIRTUALPIXELMETHOD_EDGE`|public| |4|
|`VIRTUALPIXELMETHOD_MIRROR`|public| |5|
|`VIRTUALPIXELMETHOD_TILE`|public| |7|
|`VIRTUALPIXELMETHOD_TRANSPARENT`|public| |8|
|`VIRTUALPIXELMETHOD_MASK`|public| |9|
|`VIRTUALPIXELMETHOD_BLACK`|public| |10|
|`VIRTUALPIXELMETHOD_GRAY`|public| |11|
|`VIRTUALPIXELMETHOD_WHITE`|public| |12|
|`VIRTUALPIXELMETHOD_HORIZONTALTILE`|public| |13|
|`VIRTUALPIXELMETHOD_VERTICALTILE`|public| |14|
|`VIRTUALPIXELMETHOD_HORIZONTALTILEEDGE`|public| |15|
|`VIRTUALPIXELMETHOD_VERTICALTILEEDGE`|public| |16|
|`VIRTUALPIXELMETHOD_CHECKERTILE`|public| |17|
|`PREVIEW_UNDEFINED`|public| |0|
|`PREVIEW_ROTATE`|public| |1|
|`PREVIEW_SHEAR`|public| |2|
|`PREVIEW_ROLL`|public| |3|
|`PREVIEW_HUE`|public| |4|
|`PREVIEW_SATURATION`|public| |5|
|`PREVIEW_BRIGHTNESS`|public| |6|
|`PREVIEW_GAMMA`|public| |7|
|`PREVIEW_SPIFF`|public| |8|
|`PREVIEW_DULL`|public| |9|
|`PREVIEW_GRAYSCALE`|public| |10|
|`PREVIEW_QUANTIZE`|public| |11|
|`PREVIEW_DESPECKLE`|public| |12|
|`PREVIEW_REDUCENOISE`|public| |13|
|`PREVIEW_ADDNOISE`|public| |14|
|`PREVIEW_SHARPEN`|public| |15|
|`PREVIEW_BLUR`|public| |16|
|`PREVIEW_THRESHOLD`|public| |17|
|`PREVIEW_EDGEDETECT`|public| |18|
|`PREVIEW_SPREAD`|public| |19|
|`PREVIEW_SOLARIZE`|public| |20|
|`PREVIEW_SHADE`|public| |21|
|`PREVIEW_RAISE`|public| |22|
|`PREVIEW_SEGMENT`|public| |23|
|`PREVIEW_SWIRL`|public| |24|
|`PREVIEW_IMPLODE`|public| |25|
|`PREVIEW_WAVE`|public| |26|
|`PREVIEW_OILPAINT`|public| |27|
|`PREVIEW_CHARCOALDRAWING`|public| |28|
|`PREVIEW_JPEG`|public| |29|
|`RENDERINGINTENT_UNDEFINED`|public| |0|
|`RENDERINGINTENT_SATURATION`|public| |1|
|`RENDERINGINTENT_PERCEPTUAL`|public| |2|
|`RENDERINGINTENT_ABSOLUTE`|public| |3|
|`RENDERINGINTENT_RELATIVE`|public| |4|
|`INTERLACE_UNDEFINED`|public| |0|
|`INTERLACE_NO`|public| |1|
|`INTERLACE_LINE`|public| |2|
|`INTERLACE_PLANE`|public| |3|
|`INTERLACE_PARTITION`|public| |4|
|`INTERLACE_GIF`|public| |5|
|`INTERLACE_JPEG`|public| |6|
|`INTERLACE_PNG`|public| |7|
|`FILLRULE_UNDEFINED`|public| |0|
|`FILLRULE_EVENODD`|public| |1|
|`FILLRULE_NONZERO`|public| |2|
|`PATHUNITS_UNDEFINED`|public| |0|
|`PATHUNITS_USERSPACE`|public| |1|
|`PATHUNITS_USERSPACEONUSE`|public| |2|
|`PATHUNITS_OBJECTBOUNDINGBOX`|public| |3|
|`LINECAP_UNDEFINED`|public| |0|
|`LINECAP_BUTT`|public| |1|
|`LINECAP_ROUND`|public| |2|
|`LINECAP_SQUARE`|public| |3|
|`LINEJOIN_UNDEFINED`|public| |0|
|`LINEJOIN_MITER`|public| |1|
|`LINEJOIN_ROUND`|public| |2|
|`LINEJOIN_BEVEL`|public| |3|
|`RESOURCETYPE_UNDEFINED`|public| |0|
|`RESOURCETYPE_AREA`|public| |1|
|`RESOURCETYPE_DISK`|public| |2|
|`RESOURCETYPE_FILE`|public| |3|
|`RESOURCETYPE_MAP`|public| |4|
|`RESOURCETYPE_MEMORY`|public| |5|
|`RESOURCETYPE_TIME`|public| |7|
|`RESOURCETYPE_THROTTLE`|public| |8|
|`RESOURCETYPE_THREAD`|public| |6|
|`DISPOSE_UNRECOGNIZED`|public| |0|
|`DISPOSE_UNDEFINED`|public| |0|
|`DISPOSE_NONE`|public| |1|
|`DISPOSE_BACKGROUND`|public| |2|
|`DISPOSE_PREVIOUS`|public| |3|
|`INTERPOLATE_UNDEFINED`|public| |0|
|`INTERPOLATE_AVERAGE`|public| |1|
|`INTERPOLATE_BICUBIC`|public| |2|
|`INTERPOLATE_BILINEAR`|public| |3|
|`INTERPOLATE_FILTER`|public| |4|
|`INTERPOLATE_INTEGER`|public| |5|
|`INTERPOLATE_MESH`|public| |6|
|`INTERPOLATE_NEARESTNEIGHBOR`|public| |7|
|`INTERPOLATE_SPLINE`|public| |8|
|`LAYERMETHOD_UNDEFINED`|public| |0|
|`LAYERMETHOD_COALESCE`|public| |1|
|`LAYERMETHOD_COMPAREANY`|public| |2|
|`LAYERMETHOD_COMPARECLEAR`|public| |3|
|`LAYERMETHOD_COMPAREOVERLAY`|public| |4|
|`LAYERMETHOD_DISPOSE`|public| |5|
|`LAYERMETHOD_OPTIMIZE`|public| |6|
|`LAYERMETHOD_OPTIMIZEPLUS`|public| |8|
|`LAYERMETHOD_OPTIMIZETRANS`|public| |9|
|`LAYERMETHOD_COMPOSITE`|public| |12|
|`LAYERMETHOD_OPTIMIZEIMAGE`|public| |7|
|`LAYERMETHOD_REMOVEDUPS`|public| |10|
|`LAYERMETHOD_REMOVEZERO`|public| |11|
|`LAYERMETHOD_TRIMBOUNDS`|public| |16|
|`ORIENTATION_UNDEFINED`|public| |0|
|`ORIENTATION_TOPLEFT`|public| |1|
|`ORIENTATION_TOPRIGHT`|public| |2|
|`ORIENTATION_BOTTOMRIGHT`|public| |3|
|`ORIENTATION_BOTTOMLEFT`|public| |4|
|`ORIENTATION_LEFTTOP`|public| |5|
|`ORIENTATION_RIGHTTOP`|public| |6|
|`ORIENTATION_RIGHTBOTTOM`|public| |7|
|`ORIENTATION_LEFTBOTTOM`|public| |8|
|`DISTORTION_UNDEFINED`|public| |0|
|`DISTORTION_AFFINE`|public| |1|
|`DISTORTION_AFFINEPROJECTION`|public| |2|
|`DISTORTION_ARC`|public| |9|
|`DISTORTION_BILINEAR`|public| |6|
|`DISTORTION_PERSPECTIVE`|public| |4|
|`DISTORTION_PERSPECTIVEPROJECTION`|public| |5|
|`DISTORTION_SCALEROTATETRANSLATE`|public| |3|
|`DISTORTION_POLYNOMIAL`|public| |8|
|`DISTORTION_POLAR`|public| |10|
|`DISTORTION_DEPOLAR`|public| |11|
|`DISTORTION_BARREL`|public| |14|
|`DISTORTION_SHEPARDS`|public| |16|
|`DISTORTION_SENTINEL`|public| |18|
|`DISTORTION_BARRELINVERSE`|public| |15|
|`DISTORTION_BILINEARFORWARD`|public| |6|
|`DISTORTION_BILINEARREVERSE`|public| |7|
|`DISTORTION_RESIZE`|public| |17|
|`DISTORTION_CYLINDER2PLANE`|public| |12|
|`DISTORTION_PLANE2CYLINDER`|public| |13|
|`LAYERMETHOD_MERGE`|public| |13|
|`LAYERMETHOD_FLATTEN`|public| |14|
|`LAYERMETHOD_MOSAIC`|public| |15|
|`ALPHACHANNEL_ACTIVATE`|public| |1|
|`ALPHACHANNEL_RESET`|public| |7|
|`ALPHACHANNEL_SET`|public| |8|
|`ALPHACHANNEL_UNDEFINED`|public| |0|
|`ALPHACHANNEL_COPY`|public| |3|
|`ALPHACHANNEL_DEACTIVATE`|public| |4|
|`ALPHACHANNEL_EXTRACT`|public| |5|
|`ALPHACHANNEL_OPAQUE`|public| |6|
|`ALPHACHANNEL_SHAPE`|public| |9|
|`ALPHACHANNEL_TRANSPARENT`|public| |10|
|`SPARSECOLORMETHOD_UNDEFINED`|public| |0|
|`SPARSECOLORMETHOD_BARYCENTRIC`|public| |1|
|`SPARSECOLORMETHOD_BILINEAR`|public| |7|
|`SPARSECOLORMETHOD_POLYNOMIAL`|public| |8|
|`SPARSECOLORMETHOD_SPEPARDS`|public| |16|
|`SPARSECOLORMETHOD_VORONOI`|public| |18|
|`SPARSECOLORMETHOD_INVERSE`|public| |19|
|`DITHERMETHOD_UNDEFINED`|public| |0|
|`DITHERMETHOD_NO`|public| |1|
|`DITHERMETHOD_RIEMERSMA`|public| |2|
|`DITHERMETHOD_FLOYDSTEINBERG`|public| |3|
|`FUNCTION_UNDEFINED`|public| |0|
|`FUNCTION_POLYNOMIAL`|public| |1|
|`FUNCTION_SINUSOID`|public| |2|
|`ALPHACHANNEL_BACKGROUND`|public| |2|
|`FUNCTION_ARCSIN`|public| |3|
|`FUNCTION_ARCTAN`|public| |4|
|`ALPHACHANNEL_FLATTEN`|public| |11|
|`ALPHACHANNEL_REMOVE`|public| |12|
|`STATISTIC_GRADIENT`|public| |1|
|`STATISTIC_MAXIMUM`|public| |2|
|`STATISTIC_MEAN`|public| |3|
|`STATISTIC_MEDIAN`|public| |4|
|`STATISTIC_MINIMUM`|public| |5|
|`STATISTIC_MODE`|public| |6|
|`STATISTIC_NONPEAK`|public| |7|
|`STATISTIC_STANDARD_DEVIATION`|public| |8|
|`MORPHOLOGY_CONVOLVE`|public| |1|
|`MORPHOLOGY_CORRELATE`|public| |2|
|`MORPHOLOGY_ERODE`|public| |3|
|`MORPHOLOGY_DILATE`|public| |4|
|`MORPHOLOGY_ERODE_INTENSITY`|public| |5|
|`MORPHOLOGY_DILATE_INTENSITY`|public| |6|
|`MORPHOLOGY_DISTANCE`|public| |7|
|`MORPHOLOGY_OPEN`|public| |8|
|`MORPHOLOGY_CLOSE`|public| |9|
|`MORPHOLOGY_OPEN_INTENSITY`|public| |10|
|`MORPHOLOGY_CLOSE_INTENSITY`|public| |11|
|`MORPHOLOGY_SMOOTH`|public| |12|
|`MORPHOLOGY_EDGE_IN`|public| |13|
|`MORPHOLOGY_EDGE_OUT`|public| |14|
|`MORPHOLOGY_EDGE`|public| |15|
|`MORPHOLOGY_TOP_HAT`|public| |16|
|`MORPHOLOGY_BOTTOM_HAT`|public| |17|
|`MORPHOLOGY_HIT_AND_MISS`|public| |18|
|`MORPHOLOGY_THINNING`|public| |19|
|`MORPHOLOGY_THICKEN`|public| |20|
|`MORPHOLOGY_VORONOI`|public| |21|
|`MORPHOLOGY_ITERATIVE`|public| |22|
|`KERNEL_UNITY`|public| |1|
|`KERNEL_GAUSSIAN`|public| |2|
|`KERNEL_DIFFERENCE_OF_GAUSSIANS`|public| |3|
|`KERNEL_LAPLACIAN_OF_GAUSSIANS`|public| |4|
|`KERNEL_BLUR`|public| |5|
|`KERNEL_COMET`|public| |6|
|`KERNEL_LAPLACIAN`|public| |7|
|`KERNEL_SOBEL`|public| |8|
|`KERNEL_FREI_CHEN`|public| |9|
|`KERNEL_ROBERTS`|public| |10|
|`KERNEL_PREWITT`|public| |11|
|`KERNEL_COMPASS`|public| |12|
|`KERNEL_KIRSCH`|public| |13|
|`KERNEL_DIAMOND`|public| |14|
|`KERNEL_SQUARE`|public| |15|
|`KERNEL_RECTANGLE`|public| |16|
|`KERNEL_OCTAGON`|public| |17|
|`KERNEL_DISK`|public| |18|
|`KERNEL_PLUS`|public| |19|
|`KERNEL_CROSS`|public| |20|
|`KERNEL_RING`|public| |21|
|`KERNEL_PEAKS`|public| |22|
|`KERNEL_EDGES`|public| |23|
|`KERNEL_CORNERS`|public| |24|
|`KERNEL_DIAGONALS`|public| |25|
|`KERNEL_LINE_ENDS`|public| |26|
|`KERNEL_LINE_JUNCTIONS`|public| |27|
|`KERNEL_RIDGES`|public| |28|
|`KERNEL_CONVEX_HULL`|public| |29|
|`KERNEL_THIN_SE`|public| |30|
|`KERNEL_SKELETON`|public| |31|
|`KERNEL_CHEBYSHEV`|public| |32|
|`KERNEL_MANHATTAN`|public| |33|
|`KERNEL_OCTAGONAL`|public| |34|
|`KERNEL_EUCLIDEAN`|public| |35|
|`KERNEL_USER_DEFINED`|public| |36|
|`KERNEL_BINOMIAL`|public| |37|
|`DIRECTION_LEFT_TO_RIGHT`|public| |2|
|`DIRECTION_RIGHT_TO_LEFT`|public| |1|
|`NORMALIZE_KERNEL_NONE`|public| |0|
|`NORMALIZE_KERNEL_VALUE`|public| |8192|
|`NORMALIZE_KERNEL_CORRELATE`|public| |65536|
|`NORMALIZE_KERNEL_PERCENT`|public| |4096|


## Methods


### optimizeImageLayers

(PECL imagick 2.0.0)<br/>
Removes repeated portions of images to optimize

```php
public optimizeImageLayers(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.optimizeimagelayers.php - 

***

### compareImageLayers

(PECL imagick 2.0.0)<br/>
Returns the maximum bounding region between images

```php
public compareImageLayers(int $method): \Imagick
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$method` | **int** | &lt;p&gt;<br />One of the layer method constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.compareimagelayers.php - 

***

### pingImageBlob

(PECL imagick 2.0.0)<br/>
Quickly fetch attributes

```php
public pingImageBlob(string $image): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$image` | **string** | &lt;p&gt;<br />A string containing the image.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.pingimageblob.php - 

***

### pingImageFile

(PECL imagick 2.0.0)<br/>
Get basic image attributes in a lightweight manner

```php
public pingImageFile(resource $filehandle, string $fileName = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filehandle` | **resource** | &lt;p&gt;<br />An open filehandle to the image.<br />&lt;/p&gt; |
| `$fileName` | **string** | [optional] &lt;p&gt;<br />Optional filename for this image.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.pingimagefile.php - 

***

### transposeImage

(PECL imagick 2.0.0)<br/>
Creates a vertical mirror image

```php
public transposeImage(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.transposeimage.php - 

***

### transverseImage

(PECL imagick 2.0.0)<br/>
Creates a horizontal mirror image

```php
public transverseImage(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.transverseimage.php - 

***

### trimImage

(PECL imagick 2.0.0)<br/>
Remove edges from the image

```php
public trimImage(float $fuzz): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fuzz` | **float** | &lt;p&gt;<br />By default target must match a particular pixel color exactly.<br />However, in many cases two colors may differ by a small amount.<br />The fuzz member of image defines how much tolerance is acceptable<br />to consider two colors as the same. This parameter represents the variation<br />on the quantum range.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.trimimage.php - 

***

### waveImage

(PECL imagick 2.0.0)<br/>
Applies wave filter to the image

```php
public waveImage(float $amplitude, float $length): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$amplitude` | **float** | &lt;p&gt;<br />The amplitude of the wave.<br />&lt;/p&gt; |
| `$length` | **float** | &lt;p&gt;<br />The length of the wave.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.waveimage.php - 

***

### vignetteImage

(PECL imagick 2.0.0)<br/>
Adds vignette filter to the image

```php
public vignetteImage(float $blackPoint, float $whitePoint, int $x, int $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$blackPoint` | **float** | &lt;p&gt;<br />The black point.<br />&lt;/p&gt; |
| `$whitePoint` | **float** | &lt;p&gt;<br />The white point<br />&lt;/p&gt; |
| `$x` | **int** | &lt;p&gt;<br />X offset of the ellipse<br />&lt;/p&gt; |
| `$y` | **int** | &lt;p&gt;<br />Y offset of the ellipse<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.vignetteimage.php - 

***

### uniqueImageColors

(PECL imagick 2.0.0)<br/>
Discards all but one of any pixel color

```php
public uniqueImageColors(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.uniqueimagecolors.php - 

***

### getImageMatte

(PECL imagick 2.0.0)<br/>
Return if the image has a matte channel

```php
public getImageMatte(): bool
```









**Return Value:**

<b>TRUE</b> on success or <b>FALSE</b> on failure.




**See Also:**

* https://php.net/manual/en/imagick.getimagematte.php - 

***

### setImageMatte

(PECL imagick 2.0.0)<br/>
Sets the image matte channel

```php
public setImageMatte(bool $matte): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matte` | **bool** | &lt;p&gt;<br />True activates the matte channel and false disables it.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagematte.php - 

***

### adaptiveResizeImage

Adaptively resize image with data dependent triangulation

```php
public adaptiveResizeImage(int $columns, int $rows, bool $bestfit = false, bool $legacy = false): bool
```

If legacy is true, the calculations are done with the small rounding bug that existed in Imagick before 3.4.0.<br>
If false, the calculations should produce the same results as ImageMagick CLI does.<br>
<br>
<b>Note:</b> The behavior of the parameter bestfit changed in Imagick 3.0.0. Before this version given dimensions 400x400 an image of dimensions 200x150 would be left untouched.
In Imagick 3.0.0 and later the image would be scaled up to size 400x300 as this is the "best fit" for the given dimensions. If bestfit parameter is used both width and height must be given.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$columns` | **int** | The number of columns in the scaled image. |
| `$rows` | **int** | The number of rows in the scaled image. |
| `$bestfit` | **bool** | [optional] Whether to fit the image inside a bounding box.&lt;br&gt;<br />The behavior of the parameter bestfit changed in Imagick 3.0.0. Before this version given dimensions 400x400 an image of dimensions 200x150 would be left untouched. In Imagick 3.0.0 and later the image would be scaled up to size 400x300 as this is the &quot;best fit&quot; for the given dimensions. If bestfit parameter is used both width and height must be given. |
| `$legacy` | **bool** | [optional] Added since 3.4.0. Default value FALSE |


**Return Value:**

TRUE on success



**Throws:**
<p>Throws ImagickException on error</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.adaptiveresizeimage.php - 

***

### sketchImage

(PECL imagick 2.0.0)<br/>
Simulates a pencil sketch

```php
public sketchImage(float $radius, float $sigma, float $angle): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** | &lt;p&gt;<br />The radius of the Gaussian, in pixels, not counting the center pixel<br />&lt;/p&gt; |
| `$sigma` | **float** | &lt;p&gt;<br />The standard deviation of the Gaussian, in pixels.<br />&lt;/p&gt; |
| `$angle` | **float** | &lt;p&gt;<br />Apply the effect along this angle.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.sketchimage.php - 

***

### shadeImage

(PECL imagick 2.0.0)<br/>
Creates a 3D effect

```php
public shadeImage(bool $gray, float $azimuth, float $elevation): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$gray` | **bool** | &lt;p&gt;<br />A value other than zero shades the intensity of each pixel.<br />&lt;/p&gt; |
| `$azimuth` | **float** | &lt;p&gt;<br />Defines the light source direction.<br />&lt;/p&gt; |
| `$elevation` | **float** | &lt;p&gt;<br />Defines the light source direction.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.shadeimage.php - 

***

### getSizeOffset

(PECL imagick 2.0.0)<br/>
Returns the size offset

```php
public getSizeOffset(): int
```









**Return Value:**

the size offset associated with the Imagick object.




**See Also:**

* https://php.net/manual/en/imagick.getsizeoffset.php - 

***

### setSizeOffset

(PECL imagick 2.0.0)<br/>
Sets the size and offset of the Imagick object

```php
public setSizeOffset(int $columns, int $rows, int $offset): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$columns` | **int** | &lt;p&gt;<br />The width in pixels.<br />&lt;/p&gt; |
| `$rows` | **int** | &lt;p&gt;<br />The height in pixels.<br />&lt;/p&gt; |
| `$offset` | **int** | &lt;p&gt;<br />The image offset.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setsizeoffset.php - 

***

### adaptiveBlurImage

(PECL imagick 2.0.0)<br/>
Adds adaptive blur filter to image

```php
public adaptiveBlurImage(float $radius, float $sigma, int $channel = Imagick::CHANNEL_DEFAULT): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** | &lt;p&gt;<br />The radius of the Gaussian, in pixels, not counting the center pixel.<br />Provide a value of 0 and the radius will be chosen automagically.<br />&lt;/p&gt; |
| `$sigma` | **float** | &lt;p&gt;<br />The standard deviation of the Gaussian, in pixels.<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To apply to more than one channel, combine channel constants using bitwise operators. Defaults to &lt;b&gt;Imagick::CHANNEL_DEFAULT&lt;/b&gt;. Refer to this list of channel constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.adaptiveblurimage.php - 

***

### contrastStretchImage

(PECL imagick 2.0.0)<br/>
Enhances the contrast of a color image

```php
public contrastStretchImage(float $black_point, float $white_point, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$black_point` | **float** | &lt;p&gt;<br />The black point.<br />&lt;/p&gt; |
| `$white_point` | **float** | &lt;p&gt;<br />The white point.<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. &lt;b&gt;Imagick::CHANNEL_ALL&lt;/b&gt;. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.contraststretchimage.php - 

***

### adaptiveSharpenImage

(PECL imagick 2.0.0)<br/>
Adaptively sharpen the image

```php
public adaptiveSharpenImage(float $radius, float $sigma, int $channel = Imagick::CHANNEL_DEFAULT): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** | &lt;p&gt;<br />The radius of the Gaussian, in pixels, not counting the center pixel. Use 0 for auto-select.<br />&lt;/p&gt; |
| `$sigma` | **float** | &lt;p&gt;<br />The standard deviation of the Gaussian, in pixels.<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To apply to more than one channel, combine channel constants using bitwise operators. Defaults to &lt;b&gt;Imagick::CHANNEL_DEFAULT&lt;/b&gt;. Refer to this list of channel constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.adaptivesharpenimage.php - 

***

### randomThresholdImage

(PECL imagick 2.0.0)<br/>
Creates a high-contrast, two-color image

```php
public randomThresholdImage(float $low, float $high, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$low` | **float** | &lt;p&gt;<br />The low point<br />&lt;/p&gt; |
| `$high` | **float** | &lt;p&gt;<br />The high point<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.randomthresholdimage.php - 

***

### roundCornersImage



```php
public roundCornersImage(mixed $xRounding, mixed $yRounding, mixed $strokeWidth, mixed $displace, mixed $sizeCorrection): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$xRounding` | **mixed** |  |
| `$yRounding` | **mixed** |  |
| `$strokeWidth` | **mixed** | [optional] |
| `$displace` | **mixed** | [optional] |
| `$sizeCorrection` | **mixed** | [optional] |





***

### roundCorners

(PECL imagick 2.0.0)<br/>
Rounds image corners

```php
public roundCorners(float $x_rounding, float $y_rounding, float $stroke_width = 10.0, float $displace = 5.0, float $size_correction = -6.0): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x_rounding` | **float** | &lt;p&gt;<br />x rounding<br />&lt;/p&gt; |
| `$y_rounding` | **float** | &lt;p&gt;<br />y rounding<br />&lt;/p&gt; |
| `$stroke_width` | **float** | [optional] &lt;p&gt;<br />stroke width<br />&lt;/p&gt; |
| `$displace` | **float** | [optional] &lt;p&gt;<br />image displace<br />&lt;/p&gt; |
| `$size_correction` | **float** | [optional] &lt;p&gt;<br />size correction<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.roundcorners.php - 

***

### setIteratorIndex

(PECL imagick 2.0.0)<br/>
Set the iterator position

```php
public setIteratorIndex(int $index): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **int** | &lt;p&gt;<br />The position to set the iterator to<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setiteratorindex.php - 

***

### getIteratorIndex

(PECL imagick 2.0.0)<br/>
Gets the index of the current active image

```php
public getIteratorIndex(): int
```









**Return Value:**

an integer containing the index of the image in the stack.




**See Also:**

* https://php.net/manual/en/imagick.getiteratorindex.php - 

***

### transformImage

(PECL imagick 2.0.0)<br/>
Convenience method for setting crop size and the image geometry

```php
public transformImage(string $crop, string $geometry): \Imagick
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$crop` | **string** | &lt;p&gt;<br />A crop geometry string. This geometry defines a subregion of the image to crop.<br />&lt;/p&gt; |
| `$geometry` | **string** | &lt;p&gt;<br />An image geometry string. This geometry defines the final size of the image.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.transformimage.php - 

***

### setImageOpacity

(PECL imagick 2.0.0)<br/>
Sets the image opacity level

```php
public setImageOpacity(float $opacity): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$opacity` | **float** | &lt;p&gt;<br />The level of transparency: 1.0 is fully opaque and 0.0 is fully<br />transparent.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageopacity.php - 

***

### orderedPosterizeImage

(PECL imagick 2.2.2)<br/>
Performs an ordered dither

```php
public orderedPosterizeImage(string $threshold_map, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$threshold_map` | **string** | &lt;p&gt;<br />A string containing the name of the threshold dither map to use<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.orderedposterizeimage.php - 

***

### polaroidImage

(PECL imagick 2.0.0)<br/>
Simulates a Polaroid picture

```php
public polaroidImage(\ImagickDraw $properties, float $angle): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$properties` | **\ImagickDraw** | &lt;p&gt;<br />The polaroid properties<br />&lt;/p&gt; |
| `$angle` | **float** | &lt;p&gt;<br />The polaroid angle<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.polaroidimage.php - 

***

### getImageProperty

(PECL imagick 2.0.0)<br/>
Returns the named image property

```php
public getImageProperty(string $name): string|false
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | &lt;p&gt;<br />name of the property (for example Exif:DateTime)<br />&lt;/p&gt; |


**Return Value:**

a string containing the image property, false if a
property with the given name does not exist.




**See Also:**

* https://php.net/manual/en/imagick.getimageproperty.php - 

***

### setImageProperty

(PECL imagick 2.0.0)<br/>
Sets an image property

```php
public setImageProperty(string $name, string $value): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$value` | **string** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageproperty.php - 

***

### setImageInterpolateMethod

(PECL imagick 2.0.0)<br/>
Sets the image interpolate pixel method

```php
public setImageInterpolateMethod(int $method): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$method` | **int** | &lt;p&gt;<br />The method is one of the &lt;b&gt;Imagick::INTERPOLATE_*&lt;/b&gt; constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageinterpolatemethod.php - 

***

### getImageInterpolateMethod

(PECL imagick 2.0.0)<br/>
Returns the interpolation method

```php
public getImageInterpolateMethod(): int
```









**Return Value:**

the interpolate method on success.




**See Also:**

* https://php.net/manual/en/imagick.getimageinterpolatemethod.php - 

***

### linearStretchImage

(PECL imagick 2.0.0)<br/>
Stretches with saturation the image intensity

```php
public linearStretchImage(float $blackPoint, float $whitePoint): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$blackPoint` | **float** | &lt;p&gt;<br />The image black point<br />&lt;/p&gt; |
| `$whitePoint` | **float** | &lt;p&gt;<br />The image white point<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.linearstretchimage.php - 

***

### getImageLength

(PECL imagick 2.0.0)<br/>
Returns the image length in bytes

```php
public getImageLength(): int
```









**Return Value:**

an int containing the current image size.




**See Also:**

* https://php.net/manual/en/imagick.getimagelength.php - 

***

### extentImage

(No version information available, might only be in SVN)<br/>
Set image size

```php
public extentImage(int $width, int $height, int $x, int $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$width` | **int** | &lt;p&gt;<br />The new width<br />&lt;/p&gt; |
| `$height` | **int** | &lt;p&gt;<br />The new height<br />&lt;/p&gt; |
| `$x` | **int** | &lt;p&gt;<br />X position for the new size<br />&lt;/p&gt; |
| `$y` | **int** | &lt;p&gt;<br />Y position for the new size<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.extentimage.php - 

***

### getImageOrientation

(PECL imagick 2.0.0)<br/>
Gets the image orientation

```php
public getImageOrientation(): int
```









**Return Value:**

an int on success.




**See Also:**

* https://php.net/manual/en/imagick.getimageorientation.php - 

***

### setImageOrientation

(PECL imagick 2.0.0)<br/>
Sets the image orientation

```php
public setImageOrientation(int $orientation): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$orientation` | **int** | &lt;p&gt;<br />One of the orientation constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageorientation.php - 

***

### paintFloodfillImage

(PECL imagick 2.1.0)<br/>
Changes the color value of any pixel that matches target

```php
public paintFloodfillImage(mixed $fill, float $fuzz, mixed $bordercolor, int $x, int $y, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fill` | **mixed** | &lt;p&gt;<br />ImagickPixel object or a string containing the fill color<br />&lt;/p&gt; |
| `$fuzz` | **float** | &lt;p&gt;<br />The amount of fuzz. For example, set fuzz to 10 and the color red at<br />intensities of 100 and 102 respectively are now interpreted as the<br />same color for the purposes of the floodfill.<br />&lt;/p&gt; |
| `$bordercolor` | **mixed** | &lt;p&gt;<br />ImagickPixel object or a string containing the border color<br />&lt;/p&gt; |
| `$x` | **int** | &lt;p&gt;<br />X start position of the floodfill<br />&lt;/p&gt; |
| `$y` | **int** | &lt;p&gt;<br />Y start position of the floodfill<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To apply to more than one channel, combine channel constants using bitwise operators. Defaults to &lt;b&gt;Imagick::CHANNEL_DEFAULT&lt;/b&gt;. Refer to this list of channel constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.paintfloodfillimage.php - 

***

### clutImage

(PECL imagick 2.0.0)<br/>
Replaces colors in the image from a color lookup table. Optional second parameter to replace colors in a specific channel. This method is available if Imagick has been compiled against ImageMagick version 6.3.6 or newer.

```php
public clutImage(\Imagick $lookup_table, int $channel = Imagick::CHANNEL_DEFAULT): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$lookup_table` | **\Imagick** | &lt;p&gt;<br />Imagick object containing the color lookup table<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />The Channeltype<br />constant. When not supplied, default channels are replaced.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.clutimage.php - 

***

### getImageProperties

(PECL imagick 2.0.0)<br/>
Returns the image properties

```php
public getImageProperties(string $pattern = &quot;*&quot;, bool $only_names = true): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pattern` | **string** | [optional] &lt;p&gt;<br />The pattern for property names.<br />&lt;/p&gt; |
| `$only_names` | **bool** | [optional] &lt;p&gt;<br />Whether to return only property names. If &lt;b&gt;FALSE&lt;/b&gt; then also the values are returned<br />&lt;/p&gt; |


**Return Value:**

an array containing the image properties or property names.




**See Also:**

* https://php.net/manual/en/imagick.getimageproperties.php - 

***

### getImageProfiles

(PECL imagick 2.2.0)<br/>
Returns the image profiles

```php
public getImageProfiles(string $pattern = &quot;*&quot;, bool $include_values = true): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pattern` | **string** | [optional] &lt;p&gt;<br />The pattern for profile names.<br />&lt;/p&gt; |
| `$include_values` | **bool** | [optional] &lt;p&gt;<br />Whether to return only profile names. If &lt;b&gt;FALSE&lt;/b&gt; then only profile names will be returned.<br />&lt;/p&gt; |


**Return Value:**

an array containing the image profiles or profile names.




**See Also:**

* https://php.net/manual/en/imagick.getimageprofiles.php - 

***

### distortImage

(PECL imagick 2.0.1)<br/>
Distorts an image using various distortion methods

```php
public distortImage(int $method, array $arguments, bool $bestfit): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$method` | **int** | &lt;p&gt;<br />The method of image distortion. See distortion constants<br />&lt;/p&gt; |
| `$arguments` | **array** | &lt;p&gt;<br />The arguments for this distortion method<br />&lt;/p&gt; |
| `$bestfit` | **bool** | &lt;p&gt;<br />Attempt to resize destination to fit distorted source<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.distortimage.php - 

***

### writeImageFile

(No version information available, might only be in SVN)<br/>
Writes an image to a filehandle

```php
public writeImageFile(resource $filehandle): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filehandle` | **resource** | &lt;p&gt;<br />Filehandle where to write the image<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.writeimagefile.php - 

***

### writeImagesFile

(No version information available, might only be in SVN)<br/>
Writes frames to a filehandle

```php
public writeImagesFile(resource $filehandle): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filehandle` | **resource** | &lt;p&gt;<br />Filehandle where to write the images<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.writeimagesfile.php - 

***

### resetImagePage

(No version information available, might only be in SVN)<br/>
Reset image page

```php
public resetImagePage(string $page): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$page` | **string** | &lt;p&gt;<br />The page definition. For example 7168x5147+0+0<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.resetimagepage.php - 

***

### setImageClipMask

(No version information available, might only be in SVN)<br/>
Sets image clip mask

```php
public setImageClipMask(\Imagick $clip_mask): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$clip_mask` | **\Imagick** | &lt;p&gt;<br />The Imagick object containing the clip mask<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageclipmask.php - 

***

### getImageClipMask

(No version information available, might only be in SVN)<br/>
Gets image clip mask

```php
public getImageClipMask(): \Imagick
```









**Return Value:**

an Imagick object containing the clip mask.




**See Also:**

* https://php.net/manual/en/imagick.getimageclipmask.php - 

***

### animateImages

(No version information available, might only be in SVN)<br/>
Animates an image or images

```php
public animateImages(string $x_server): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x_server` | **string** | &lt;p&gt;<br />X server address<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.animateimages.php - 

***

### recolorImage

(No version information available, might only be in SVN)<br/>
Recolors image

```php
public recolorImage(array $matrix): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matrix` | **array** | &lt;p&gt;<br />The matrix containing the color values<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.recolorimage.php - 

***

### setFont

(PECL imagick 2.1.0)<br/>
Sets font

```php
public setFont(string $font): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$font` | **string** | &lt;p&gt;<br />Font name or a filename<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setfont.php - 

***

### getFont

(PECL imagick 2.1.0)<br/>
Gets font

```php
public getFont(): string|false
```









**Return Value:**

the string containing the font name or <b>FALSE</b> if not font is set.




**See Also:**

* https://php.net/manual/en/imagick.getfont.php - 

***

### setPointSize

(PECL imagick 2.1.0)<br/>
Sets point size

```php
public setPointSize(float $point_size): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$point_size` | **float** | &lt;p&gt;<br />Point size<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setpointsize.php - 

***

### getPointSize

(No version information available, might only be in SVN)<br/>
Gets point size

```php
public getPointSize(): float
```









**Return Value:**

a float containing the point size.




**See Also:**

* https://php.net/manual/en/imagick.getpointsize.php - 

***

### mergeImageLayers

(PECL imagick 2.1.0)<br/>
Merges image layers

```php
public mergeImageLayers(int $layer_method): \Imagick
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$layer_method` | **int** | &lt;p&gt;<br />One of the &lt;b&gt;Imagick::LAYERMETHOD_*&lt;/b&gt; constants<br />&lt;/p&gt; |


**Return Value:**

Returns an Imagick object containing the merged image.



**Throws:**

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.mergeimagelayers.php - 

***

### setImageAlphaChannel

(No version information available, might only be in SVN)<br/>
Sets image alpha channel

```php
public setImageAlphaChannel(int $mode): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$mode` | **int** | &lt;p&gt;<br />One of the &lt;b&gt;Imagick::ALPHACHANNEL_*&lt;/b&gt; constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagealphachannel.php - 

***

### floodFillPaintImage

(No version information available, might only be in SVN)<br/>
Changes the color value of any pixel that matches target

```php
public floodFillPaintImage(mixed $fill, float $fuzz, mixed $target, int $x, int $y, bool $invert, int $channel = Imagick::CHANNEL_DEFAULT): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fill` | **mixed** | &lt;p&gt;<br />ImagickPixel object or a string containing the fill color<br />&lt;/p&gt; |
| `$fuzz` | **float** | &lt;p&gt;<br />The amount of fuzz. For example, set fuzz to 10 and the color red at intensities of 100 and 102 respectively are now interpreted as the same color.<br />&lt;/p&gt; |
| `$target` | **mixed** | &lt;p&gt;<br />ImagickPixel object or a string containing the target color to paint<br />&lt;/p&gt; |
| `$x` | **int** | &lt;p&gt;<br />X start position of the floodfill<br />&lt;/p&gt; |
| `$y` | **int** | &lt;p&gt;<br />Y start position of the floodfill<br />&lt;/p&gt; |
| `$invert` | **bool** | &lt;p&gt;<br />If &lt;b&gt;TRUE&lt;/b&gt; paints any pixel that does not match the target color.<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To apply to more than one channel, combine channel constants using bitwise operators. Defaults to &lt;b&gt;Imagick::CHANNEL_DEFAULT&lt;/b&gt;. Refer to this list of channel constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.floodfillpaintimage.php - 

***

### opaquePaintImage

(No version information available, might only be in SVN)<br/>
Changes the color value of any pixel that matches target

```php
public opaquePaintImage(mixed $target, mixed $fill, float $fuzz, bool $invert, int $channel = Imagick::CHANNEL_DEFAULT): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$target` | **mixed** | &lt;p&gt;<br />ImagickPixel object or a string containing the color to change<br />&lt;/p&gt; |
| `$fill` | **mixed** | &lt;p&gt;<br />The replacement color<br />&lt;/p&gt; |
| `$fuzz` | **float** | &lt;p&gt;<br />The amount of fuzz. For example, set fuzz to 10 and the color red at intensities of 100 and 102 respectively are now interpreted as the same color.<br />&lt;/p&gt; |
| `$invert` | **bool** | &lt;p&gt;<br />If &lt;b&gt;TRUE&lt;/b&gt; paints any pixel that does not match the target color.<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To apply to more than one channel, combine channel constants using bitwise operators. Defaults to &lt;b&gt;Imagick::CHANNEL_DEFAULT&lt;/b&gt;. Refer to this list of channel constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.opaquepaintimage.php - 

***

### transparentPaintImage

(No version information available, might only be in SVN)<br/>
Paints pixels transparent

```php
public transparentPaintImage(mixed $target, float $alpha, float $fuzz, bool $invert): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$target` | **mixed** | &lt;p&gt;<br />The target color to paint<br />&lt;/p&gt; |
| `$alpha` | **float** | &lt;p&gt;<br />The level of transparency: 1.0 is fully opaque and 0.0 is fully transparent.<br />&lt;/p&gt; |
| `$fuzz` | **float** | &lt;p&gt;<br />The amount of fuzz. For example, set fuzz to 10 and the color red at intensities of 100 and 102 respectively are now interpreted as the same color.<br />&lt;/p&gt; |
| `$invert` | **bool** | &lt;p&gt;<br />If &lt;b&gt;TRUE&lt;/b&gt; paints any pixel that does not match the target color.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.transparentpaintimage.php - 

***

### liquidRescaleImage

(No version information available, might only be in SVN)<br/>
Animates an image or images

```php
public liquidRescaleImage(int $width, int $height, float $delta_x, float $rigidity): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$width` | **int** | &lt;p&gt;<br />The width of the target size<br />&lt;/p&gt; |
| `$height` | **int** | &lt;p&gt;<br />The height of the target size<br />&lt;/p&gt; |
| `$delta_x` | **float** | &lt;p&gt;<br />How much the seam can traverse on x-axis.<br />Passing 0 causes the seams to be straight.<br />&lt;/p&gt; |
| `$rigidity` | **float** | &lt;p&gt;<br />Introduces a bias for non-straight seams. This parameter is<br />typically 0.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.liquidrescaleimage.php - 

***

### encipherImage

(No version information available, might only be in SVN)<br/>
Enciphers an image

```php
public encipherImage(string $passphrase): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$passphrase` | **string** | &lt;p&gt;<br />The passphrase<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.encipherimage.php - 

***

### decipherImage

(No version information available, might only be in SVN)<br/>
Deciphers an image

```php
public decipherImage(string $passphrase): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$passphrase` | **string** | &lt;p&gt;<br />The passphrase<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.decipherimage.php - 

***

### setGravity

(No version information available, might only be in SVN)<br/>
Sets the gravity

```php
public setGravity(int $gravity): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$gravity` | **int** | &lt;p&gt;<br />The gravity property. Refer to the list of<br />gravity constants.<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagick.setgravity.php - 

***

### getGravity

(No version information available, might only be in SVN)<br/>
Gets the gravity

```php
public getGravity(): int
```









**Return Value:**

the gravity property. Refer to the list of
gravity constants.




**See Also:**

* https://php.net/manual/en/imagick.getgravity.php - 

***

### getImageChannelRange

(PECL imagick 2.2.1)<br/>
Gets channel range

```php
public getImageChannelRange(int $channel): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **int** | &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To apply to more than one channel, combine channel constants using bitwise operators. Defaults to &lt;b&gt;Imagick::CHANNEL_DEFAULT&lt;/b&gt;. Refer to this list of channel constants<br />&lt;/p&gt; |


**Return Value:**

an array containing minima and maxima values of the channel(s).




**See Also:**

* https://php.net/manual/en/imagick.getimagechannelrange.php - 

***

### getImageAlphaChannel

(No version information available, might only be in SVN)<br/>
Gets the image alpha channel

```php
public getImageAlphaChannel(): int
```









**Return Value:**

a constant defining the current alpha channel value. Refer to this
list of alpha channel constants.




**See Also:**

* https://php.net/manual/en/imagick.getimagealphachannel.php - 

***

### getImageChannelDistortions

(No version information available, might only be in SVN)<br/>
Gets channel distortions

```php
public getImageChannelDistortions(\Imagick $reference, int $metric, int $channel = Imagick::CHANNEL_DEFAULT): float
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reference` | **\Imagick** | &lt;p&gt;<br />Imagick object containing the reference image<br />&lt;/p&gt; |
| `$metric` | **int** | &lt;p&gt;<br />Refer to this list of metric type constants.<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To apply to more than one channel, combine channel constants using bitwise operators. Defaults to &lt;b&gt;Imagick::CHANNEL_DEFAULT&lt;/b&gt;. Refer to this list of channel constants<br />&lt;/p&gt; |


**Return Value:**

a float describing the channel distortion.




**See Also:**

* https://php.net/manual/en/imagick.getimagechanneldistortions.php - 

***

### setImageGravity

(No version information available, might only be in SVN)<br/>
Sets the image gravity

```php
public setImageGravity(int $gravity): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$gravity` | **int** | &lt;p&gt;<br />The gravity property. Refer to the list of<br />gravity constants.<br />&lt;/p&gt; |


**Return Value:**

No value is returned.




**See Also:**

* https://php.net/manual/en/imagick.setimagegravity.php - 

***

### getImageGravity

(No version information available, might only be in SVN)<br/>
Gets the image gravity

```php
public getImageGravity(): int
```









**Return Value:**

the images gravity property. Refer to the list of
gravity constants.




**See Also:**

* https://php.net/manual/en/imagick.getimagegravity.php - 

***

### importImagePixels

(No version information available, might only be in SVN)<br/>
Imports image pixels

```php
public importImagePixels(int $x, int $y, int $width, int $height, string $map, int $storage, array $pixels): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **int** | &lt;p&gt;<br />The image x position<br />&lt;/p&gt; |
| `$y` | **int** | &lt;p&gt;<br />The image y position<br />&lt;/p&gt; |
| `$width` | **int** | &lt;p&gt;<br />The image width<br />&lt;/p&gt; |
| `$height` | **int** | &lt;p&gt;<br />The image height<br />&lt;/p&gt; |
| `$map` | **string** | &lt;p&gt;<br />Map of pixel ordering as a string. This can be for example RGB.<br />The value can be any combination or order of R = red, G = green, B = blue, A = alpha (0 is transparent),<br />O = opacity (0 is opaque), C = cyan, Y = yellow, M = magenta, K = black, I = intensity (for grayscale), P = pad.<br />&lt;/p&gt; |
| `$storage` | **int** | &lt;p&gt;<br />The pixel storage method.<br />Refer to this list of pixel constants.<br />&lt;/p&gt; |
| `$pixels` | **array** | &lt;p&gt;<br />The array of pixels<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.importimagepixels.php - 

***

### deskewImage

(No version information available, might only be in SVN)<br/>
Removes skew from the image

```php
public deskewImage(float $threshold): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$threshold` | **float** | &lt;p&gt;<br />Deskew threshold<br />&lt;/p&gt; |





**See Also:**

* https://php.net/manual/en/imagick.deskewimage.php - 

***

### segmentImage

(No version information available, might only be in SVN)<br/>
Segments an image

```php
public segmentImage(int $COLORSPACE, float $cluster_threshold, float $smooth_threshold, bool $verbose = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$COLORSPACE` | **int** | &lt;p&gt;<br />One of the COLORSPACE constants.<br />&lt;/p&gt; |
| `$cluster_threshold` | **float** | &lt;p&gt;<br />A percentage describing minimum number of pixels<br />contained in hexedra before it is considered valid.<br />&lt;/p&gt; |
| `$smooth_threshold` | **float** | &lt;p&gt;<br />Eliminates noise from the histogram.<br />&lt;/p&gt; |
| `$verbose` | **bool** | [optional] &lt;p&gt;<br />Whether to output detailed information about recognised classes.<br />&lt;/p&gt; |





**See Also:**

* https://php.net/manual/en/imagick.segmentimage.php - 

***

### sparseColorImage

(No version information available, might only be in SVN)<br/>
Interpolates colors

```php
public sparseColorImage(int $SPARSE_METHOD, array $arguments, int $channel = Imagick::CHANNEL_DEFAULT): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$SPARSE_METHOD` | **int** | &lt;p&gt;<br />Refer to this list of sparse method constants<br />&lt;/p&gt; |
| `$arguments` | **array** | &lt;p&gt;<br />An array containing the coordinates.<br />The array is in format array(1,1, 2,45)<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.sparsecolorimage.php - 

***

### remapImage

(No version information available, might only be in SVN)<br/>
Remaps image colors

```php
public remapImage(\Imagick $replacement, int $DITHER): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$replacement` | **\Imagick** | &lt;p&gt;<br />An Imagick object containing the replacement colors<br />&lt;/p&gt; |
| `$DITHER` | **int** | &lt;p&gt;<br />Refer to this list of dither method constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.remapimage.php - 

***

### exportImagePixels

(No version information available, might only be in SVN)<br/>
Exports raw image pixels

```php
public exportImagePixels(int $x, int $y, int $width, int $height, string $map, int $STORAGE): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **int** | &lt;p&gt;<br />X-coordinate of the exported area<br />&lt;/p&gt; |
| `$y` | **int** | &lt;p&gt;<br />Y-coordinate of the exported area<br />&lt;/p&gt; |
| `$width` | **int** | &lt;p&gt;<br />Width of the exported aread<br />&lt;/p&gt; |
| `$height` | **int** | &lt;p&gt;<br />Height of the exported area<br />&lt;/p&gt; |
| `$map` | **string** | &lt;p&gt;<br />Ordering of the exported pixels. For example &quot;RGB&quot;.<br />Valid characters for the map are R, G, B, A, O, C, Y, M, K, I and P.<br />&lt;/p&gt; |
| `$STORAGE` | **int** | &lt;p&gt;<br />Refer to this list of pixel type constants<br />&lt;/p&gt; |


**Return Value:**

an array containing the pixels values.




**See Also:**

* https://php.net/manual/en/imagick.exportimagepixels.php - 

***

### getImageChannelKurtosis

(No version information available, might only be in SVN)<br/>
The getImageChannelKurtosis purpose

```php
public getImageChannelKurtosis(int $channel = Imagick::CHANNEL_DEFAULT): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To apply to more than one channel, combine channel constants using bitwise operators. Defaults to &lt;b&gt;Imagick::CHANNEL_DEFAULT&lt;/b&gt;. Refer to this list of channel constants<br />&lt;/p&gt; |


**Return Value:**

an array with kurtosis and skewness
members.




**See Also:**

* https://php.net/manual/en/imagick.getimagechannelkurtosis.php - 

***

### functionImage

(No version information available, might only be in SVN)<br/>
Applies a function on the image

```php
public functionImage(int $function, array $arguments, int $channel = Imagick::CHANNEL_DEFAULT): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$function` | **int** | &lt;p&gt;<br />Refer to this list of function constants<br />&lt;/p&gt; |
| `$arguments` | **array** | &lt;p&gt;<br />Array of arguments to pass to this function.<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.functionimage.php - 

***

### transformImageColorspace



```php
public transformImageColorspace(mixed $COLORSPACE): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$COLORSPACE` | **mixed** |  |





***

### haldClutImage

(No version information available, might only be in SVN)<br/>
Replaces colors in the image

```php
public haldClutImage(\Imagick $clut, int $channel = Imagick::CHANNEL_DEFAULT): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$clut` | **\Imagick** | &lt;p&gt;<br />Imagick object containing the Hald lookup image.<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To apply to more than one channel, combine channel constants using bitwise operators. Defaults to &lt;b&gt;Imagick::CHANNEL_DEFAULT&lt;/b&gt;. Refer to this list of channel constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.haldclutimage.php - 

***

### autoLevelImage



```php
public autoLevelImage(mixed $CHANNEL): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$CHANNEL` | **mixed** | [optional] |





***

### blueShiftImage



```php
public blueShiftImage(mixed $factor): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$factor` | **mixed** | [optional] |





***

### getImageArtifact

(No version information available, might only be in SVN)<br/>
Get image artifact

```php
public getImageArtifact(string $artifact): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$artifact` | **string** | &lt;p&gt;<br />The name of the artifact<br />&lt;/p&gt; |


**Return Value:**

the artifact value on success.




**See Also:**

* https://php.net/manual/en/imagick.getimageartifact.php - 

***

### setImageArtifact

(No version information available, might only be in SVN)<br/>
Set image artifact

```php
public setImageArtifact(string $artifact, string $value): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$artifact` | **string** | &lt;p&gt;<br />The name of the artifact<br />&lt;/p&gt; |
| `$value` | **string** | &lt;p&gt;<br />The value of the artifact<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageartifact.php - 

***

### deleteImageArtifact

(No version information available, might only be in SVN)<br/>
Delete image artifact

```php
public deleteImageArtifact(string $artifact): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$artifact` | **string** | &lt;p&gt;<br />The name of the artifact to delete<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.deleteimageartifact.php - 

***

### getColorspace

(PECL imagick 0.9.10-0.9.9)<br/>
Gets the colorspace

```php
public getColorspace(): int
```









**Return Value:**

an integer which can be compared against COLORSPACE constants.




**See Also:**

* https://php.net/manual/en/imagick.getcolorspace.php - 

***

### setColorspace

(No version information available, might only be in SVN)<br/>
Set colorspace

```php
public setColorspace(int $COLORSPACE): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$COLORSPACE` | **int** | &lt;p&gt;<br />One of the COLORSPACE constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setcolorspace.php - 

***

### clampImage



```php
public clampImage(mixed $CHANNEL): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$CHANNEL` | **mixed** | [optional] |





***

### smushImages



```php
public smushImages(mixed $stack, mixed $offset): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stack` | **mixed** |  |
| `$offset` | **mixed** |  |





***

### __construct

(PECL imagick 2.0.0)<br/>
The Imagick constructor

```php
public __construct(mixed $files = null): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$files` | **mixed** | &lt;p&gt;<br />The path to an image to load or an array of paths. Paths can include<br />wildcards for file names, or can be URLs.<br />&lt;/p&gt; |




**Throws:**
<p>Throws ImagickException on error.</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.construct.php - 

***

### __toString



```php
public __toString(): string
```












***

### count



```php
public count(): mixed
```












***

### getPixelIterator

(PECL imagick 2.0.0)<br/>
Returns a MagickPixelIterator

```php
public getPixelIterator(): \ImagickPixelIterator
```









**Return Value:**

an ImagickPixelIterator on success.




**See Also:**

* https://php.net/manual/en/imagick.getpixeliterator.php - 

***

### getPixelRegionIterator

(PECL imagick 2.0.0)<br/>
Get an ImagickPixelIterator for an image section

```php
public getPixelRegionIterator(int $x, int $y, int $columns, int $rows): \ImagickPixelIterator
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **int** | &lt;p&gt;<br />The x-coordinate of the region.<br />&lt;/p&gt; |
| `$y` | **int** | &lt;p&gt;<br />The y-coordinate of the region.<br />&lt;/p&gt; |
| `$columns` | **int** | &lt;p&gt;<br />The width of the region.<br />&lt;/p&gt; |
| `$rows` | **int** | &lt;p&gt;<br />The height of the region.<br />&lt;/p&gt; |


**Return Value:**

an ImagickPixelIterator for an image section.




**See Also:**

* https://php.net/manual/en/imagick.getpixelregioniterator.php - 

***

### readImage

(PECL imagick 0.9.0-0.9.9)<br/>
Reads image from filename

```php
public readImage(string $filename): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |


**Return Value:**

<b>TRUE</b> on success.



**Throws:**
<p>Throws ImagickException on error.</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.readimage.php - 

***

### readImages



```php
public readImages(mixed $filenames): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filenames` | **mixed** |  |




**Throws:**
<p>Throws ImagickException on error.</p>

- [`ImagickException`](./ImagickException.md)



***

### readImageBlob

(PECL imagick 2.0.0)<br/>
Reads image from a binary string

```php
public readImageBlob(string $image, string $filename = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$image` | **string** |  |
| `$filename` | **string** | [optional] |


**Return Value:**

<b>TRUE</b> on success.



**Throws:**
<p>Throws ImagickException on error.</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.readimageblob.php - 

***

### setImageFormat

(PECL imagick 2.0.0)<br/>
Sets the format of a particular image

```php
public setImageFormat(string $format): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$format` | **string** | &lt;p&gt;<br />String presentation of the image format. Format support<br />depends on the ImageMagick installation.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageformat.php - 

***

### scaleImage

Scales the size of an image to the given dimensions. Passing zero as either of the arguments will preserve dimension while scaling.<br>
If legacy is true, the calculations are done with the small rounding bug that existed in Imagick before 3.4.0.<br>
If false, the calculations should produce the same results as ImageMagick CLI does.

```php
public scaleImage(int $cols, int $rows, bool $bestfit = false, bool $legacy = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cols` | **int** |  |
| `$rows` | **int** |  |
| `$bestfit` | **bool** | [optional] The behavior of the parameter bestfit changed in Imagick 3.0.0. Before this version given dimensions 400x400 an image of dimensions 200x150 would be left untouched. In Imagick 3.0.0 and later the image would be scaled up to size 400x300 as this is the &quot;best fit&quot; for the given dimensions. If bestfit parameter is used both width and height must be given. |
| `$legacy` | **bool** | [optional] Added since 3.4.0. Default value FALSE |


**Return Value:**

<b>TRUE</b> on success.



**Throws:**
<p>Throws ImagickException on error</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.scaleimage.php - 

***

### writeImage

(PECL imagick 0.9.0-0.9.9)<br/>
Writes an image to the specified filename

```php
public writeImage(string $filename = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** | [optional] &lt;p&gt;<br />Filename where to write the image. The extension of the filename<br />defines the type of the file.<br />Format can be forced regardless of file extension using format: prefix,<br />for example &quot;jpg:test.png&quot;.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.writeimage.php - 

***

### writeImages

(PECL imagick 0.9.0-0.9.9)<br/>
Writes an image or image sequence

```php
public writeImages(string $filename, bool $adjoin): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |
| `$adjoin` | **bool** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.writeimages.php - 

***

### blurImage

(PECL imagick 2.0.0)<br/>
Adds blur filter to image

```php
public blurImage(float $radius, float $sigma, int $channel = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** | &lt;p&gt;<br />Blur radius<br />&lt;/p&gt; |
| `$sigma` | **float** | &lt;p&gt;<br />Standard deviation<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />The Channeltype<br />constant. When not supplied, all channels are blurred.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.blurimage.php - 

***

### thumbnailImage

Changes the size of an image to the given dimensions and removes any associated profiles.<br>
If legacy is true, the calculations are done with the small rounding bug that existed in Imagick before 3.4.0.<br>
If false, the calculations should produce the same results as ImageMagick CLI does.<br>
<br>
<b>Note:</b> The behavior of the parameter bestfit changed in Imagick 3.0.0. Before this version given dimensions 400x400 an image of dimensions 200x150 would be left untouched. In Imagick 3.0.0 and later the image would be scaled up to size 400x300 as this is the "best fit" for the given dimensions. If bestfit parameter is used both width and height must be given.

```php
public thumbnailImage(int $columns, int $rows, bool $bestfit = false, bool $fill = false, bool $legacy = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$columns` | **int** | &lt;p&gt;<br />Image width<br />&lt;/p&gt; |
| `$rows` | **int** | &lt;p&gt;<br />Image height<br />&lt;/p&gt; |
| `$bestfit` | **bool** | [optional] &lt;p&gt;<br />Whether to force maximum values<br />&lt;/p&gt;<br />The behavior of the parameter bestfit changed in Imagick 3.0.0. Before this version given dimensions 400x400 an image of dimensions 200x150 would be left untouched. In Imagick 3.0.0 and later the image would be scaled up to size 400x300 as this is the &quot;best fit&quot; for the given dimensions. If bestfit parameter is used both width and height must be given. |
| `$fill` | **bool** | [optional] |
| `$legacy` | **bool** | [optional] Added since 3.4.0. Default value FALSE |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.thumbnailimage.php - 

***

### cropThumbnailImage

Creates a cropped thumbnail at the requested size.

```php
public cropThumbnailImage(int $width, int $height, bool $legacy = false): bool
```

If legacy is true, uses the incorrect behaviour that was present until Imagick 3.4.0.
If false it uses the correct behaviour.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$width` | **int** | The width of the thumbnail |
| `$height` | **int** | The Height of the thumbnail |
| `$legacy` | **bool** | [optional] Added since 3.4.0. Default value FALSE |


**Return Value:**

TRUE on succes



**Throws:**
<p>Throws ImagickException on error</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.cropthumbnailimage.php - 

***

### getImageFilename

(PECL imagick 2.0.0)<br/>
Returns the filename of a particular image in a sequence

```php
public getImageFilename(): string
```









**Return Value:**

a string with the filename of the image.




**See Also:**

* https://php.net/manual/en/imagick.getimagefilename.php - 

***

### setImageFilename

(PECL imagick 2.0.0)<br/>
Sets the filename of a particular image

```php
public setImageFilename(string $filename): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagefilename.php - 

***

### getImageFormat

(PECL imagick 2.0.0)<br/>
Returns the format of a particular image in a sequence

```php
public getImageFormat(): string
```









**Return Value:**

a string containing the image format on success.




**See Also:**

* https://php.net/manual/en/imagick.getimageformat.php - 

***

### getImageMimeType



```php
public getImageMimeType(): string
```









**Return Value:**

Returns the image mime-type.




**See Also:**

* https://secure.php.net/manual/en/imagick.getimagemimetype.php - 

***

### removeImage

(PECL imagick 2.0.0)<br/>
Removes an image from the image list

```php
public removeImage(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.removeimage.php - 

***

### destroy

(PECL imagick 2.0.0)<br/>
Destroys the Imagick object

```php
public destroy(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.destroy.php - 

***

### clear

(PECL imagick 2.0.0)<br/>
Clears all resources associated to Imagick object

```php
public clear(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.clear.php - 

***

### getImageSize

(PECL imagick 2.0.0)<br/>
Returns the image length in bytes

```php
public getImageSize(): int
```






* **Warning:** this method is **deprecated**. This means that this method will likely be removed in a future version.




**Return Value:**

an int containing the current image size.




**See Also:**

* https://php.net/manual/en/imagick.getimagesize.php - 

***

### getImageBlob

(PECL imagick 2.0.0)<br/>
Returns the image sequence as a blob

```php
public getImageBlob(): string
```









**Return Value:**

a string containing the image.




**See Also:**

* https://php.net/manual/en/imagick.getimageblob.php - 

***

### getImagesBlob

(PECL imagick 2.0.0)<br/>
Returns all image sequences as a blob

```php
public getImagesBlob(): string
```









**Return Value:**

a string containing the images. On failure, throws ImagickException on failure



**Throws:**
<p>on failure</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.getimagesblob.php - 

***

### setFirstIterator

(PECL imagick 2.0.0)<br/>
Sets the Imagick iterator to the first image

```php
public setFirstIterator(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setfirstiterator.php - 

***

### setLastIterator

(PECL imagick 2.0.1)<br/>
Sets the Imagick iterator to the last image

```php
public setLastIterator(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setlastiterator.php - 

***

### resetIterator



```php
public resetIterator(): mixed
```












***

### previousImage

(PECL imagick 2.0.0)<br/>
Move to the previous image in the object

```php
public previousImage(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.previousimage.php - 

***

### nextImage

(PECL imagick 2.0.0)<br/>
Moves to the next image

```php
public nextImage(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.nextimage.php - 

***

### hasPreviousImage

(PECL imagick 2.0.0)<br/>
Checks if the object has a previous image

```php
public hasPreviousImage(): bool
```









**Return Value:**

<b>TRUE</b> if the object has more images when traversing the list in the
reverse direction, returns <b>FALSE</b> if there are none.




**See Also:**

* https://php.net/manual/en/imagick.haspreviousimage.php - 

***

### hasNextImage

(PECL imagick 2.0.0)<br/>
Checks if the object has more images

```php
public hasNextImage(): bool
```









**Return Value:**

<b>TRUE</b> if the object has more images when traversing the list in the
forward direction, returns <b>FALSE</b> if there are none.




**See Also:**

* https://php.net/manual/en/imagick.hasnextimage.php - 

***

### setImageIndex

(PECL imagick 2.0.0)<br/>
Set the iterator position

```php
public setImageIndex(int $index): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **int** | &lt;p&gt;<br />The position to set the iterator to<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageindex.php - 

***

### getImageIndex

(PECL imagick 2.0.0)<br/>
Gets the index of the current active image

```php
public getImageIndex(): int
```









**Return Value:**

an integer containing the index of the image in the stack.




**See Also:**

* https://php.net/manual/en/imagick.getimageindex.php - 

***

### commentImage

(PECL imagick 2.0.0)<br/>
Adds a comment to your image

```php
public commentImage(string $comment): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$comment` | **string** | &lt;p&gt;<br />The comment to add<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.commentimage.php - 

***

### cropImage

(PECL imagick 2.0.0)<br/>
Extracts a region of the image

```php
public cropImage(int $width, int $height, int $x, int $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$width` | **int** | &lt;p&gt;<br />The width of the crop<br />&lt;/p&gt; |
| `$height` | **int** | &lt;p&gt;<br />The height of the crop<br />&lt;/p&gt; |
| `$x` | **int** | &lt;p&gt;<br />The X coordinate of the cropped region&#039;s top left corner<br />&lt;/p&gt; |
| `$y` | **int** | &lt;p&gt;<br />The Y coordinate of the cropped region&#039;s top left corner<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.cropimage.php - 

***

### labelImage

(PECL imagick 2.0.0)<br/>
Adds a label to an image

```php
public labelImage(string $label): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$label` | **string** | &lt;p&gt;<br />The label to add<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.labelimage.php - 

***

### getImageGeometry

(PECL imagick 2.0.0)<br/>
Gets the width and height as an associative array

```php
public getImageGeometry(): array
```









**Return Value:**

an array with the width/height of the image.




**See Also:**

* https://php.net/manual/en/imagick.getimagegeometry.php - 

***

### drawImage

(PECL imagick 2.0.0)<br/>
Renders the ImagickDraw object on the current image

```php
public drawImage(\ImagickDraw $draw): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$draw` | **\ImagickDraw** | &lt;p&gt;<br />The drawing operations to render on the image.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.drawimage.php - 

***

### setImageCompressionQuality

(No version information available, might only be in SVN)<br/>
Sets the image compression quality

```php
public setImageCompressionQuality(int $quality): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$quality` | **int** | &lt;p&gt;<br />The image compression quality as an integer<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagecompressionquality.php - 

***

### getImageCompressionQuality

(PECL imagick 2.2.2)<br/>
Gets the current image's compression quality

```php
public getImageCompressionQuality(): int
```









**Return Value:**

integer describing the images compression quality




**See Also:**

* https://php.net/manual/en/imagick.getimagecompressionquality.php - 

***

### annotateImage

(PECL imagick 2.0.0)<br/>
Annotates an image with text

```php
public annotateImage(\ImagickDraw $draw_settings, float $x, float $y, float $angle, string $text): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$draw_settings` | **\ImagickDraw** | &lt;p&gt;<br />The ImagickDraw object that contains settings for drawing the text<br />&lt;/p&gt; |
| `$x` | **float** | &lt;p&gt;<br />Horizontal offset in pixels to the left of text<br />&lt;/p&gt; |
| `$y` | **float** | &lt;p&gt;<br />Vertical offset in pixels to the baseline of text<br />&lt;/p&gt; |
| `$angle` | **float** | &lt;p&gt;<br />The angle at which to write the text<br />&lt;/p&gt; |
| `$text` | **string** | &lt;p&gt;<br />The string to draw<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.annotateimage.php - 

***

### compositeImage

(PECL imagick 2.0.0)<br/>
Composite one image onto another

```php
public compositeImage(\Imagick $composite_object, int $composite, int $x, int $y, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$composite_object` | **\Imagick** | &lt;p&gt;<br />Imagick object which holds the composite image<br />&lt;/p&gt; |
| `$composite` | **int** | Composite operator |
| `$x` | **int** | &lt;p&gt;<br />The column offset of the composited image<br />&lt;/p&gt; |
| `$y` | **int** | &lt;p&gt;<br />The row offset of the composited image<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.compositeimage.php - 

***

### modulateImage

(PECL imagick 2.0.0)<br/>
Control the brightness, saturation, and hue

```php
public modulateImage(float $brightness, float $saturation, float $hue): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$brightness` | **float** |  |
| `$saturation` | **float** |  |
| `$hue` | **float** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.modulateimage.php - 

***

### getImageColors

(PECL imagick 2.0.0)<br/>
Gets the number of unique colors in the image

```php
public getImageColors(): int
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.getimagecolors.php - 

***

### montageImage

(PECL imagick 2.0.0)<br/>
Creates a composite image

```php
public montageImage(\ImagickDraw $draw, string $tile_geometry, string $thumbnail_geometry, int $mode, string $frame): \Imagick
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$draw` | **\ImagickDraw** | &lt;p&gt;<br />The font name, size, and color are obtained from this object.<br />&lt;/p&gt; |
| `$tile_geometry` | **string** | &lt;p&gt;<br />The number of tiles per row and page (e.g. 6x4+0+0).<br />&lt;/p&gt; |
| `$thumbnail_geometry` | **string** | &lt;p&gt;<br />Preferred image size and border size of each thumbnail<br />(e.g. 120x120+4+3&gt;).<br />&lt;/p&gt; |
| `$mode` | **int** | &lt;p&gt;<br />Thumbnail framing mode, see Montage Mode constants.<br />&lt;/p&gt; |
| `$frame` | **string** | &lt;p&gt;<br />Surround the image with an ornamental border (e.g. 15x15+3+3). The<br />frame color is that of the thumbnail&#039;s matte color.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.montageimage.php - 

***

### identifyImage

(PECL imagick 2.0.0)<br/>
Identifies an image and fetches attributes

```php
public identifyImage(bool $appendRawOutput = false): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$appendRawOutput` | **bool** | [optional] |


**Return Value:**

Identifies an image and returns the attributes. Attributes include
the image width, height, size, and others.




**See Also:**

* https://php.net/manual/en/imagick.identifyimage.php - 

***

### thresholdImage

(PECL imagick 2.0.0)<br/>
Changes the value of individual pixels based on a threshold

```php
public thresholdImage(float $threshold, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$threshold` | **float** |  |
| `$channel` | **int** | [optional] |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.thresholdimage.php - 

***

### adaptiveThresholdImage

(PECL imagick 2.0.0)<br/>
Selects a threshold for each pixel based on a range of intensity

```php
public adaptiveThresholdImage(int $width, int $height, int $offset): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$width` | **int** | &lt;p&gt;<br />Width of the local neighborhood.<br />&lt;/p&gt; |
| `$height` | **int** | &lt;p&gt;<br />Height of the local neighborhood.<br />&lt;/p&gt; |
| `$offset` | **int** | &lt;p&gt;<br />The mean offset<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.adaptivethresholdimage.php - 

***

### blackThresholdImage

(PECL imagick 2.0.0)<br/>
Forces all pixels below the threshold into black

```php
public blackThresholdImage(mixed $threshold): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$threshold` | **mixed** | &lt;p&gt;<br />The threshold below which everything turns black<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.blackthresholdimage.php - 

***

### whiteThresholdImage

(PECL imagick 2.0.0)<br/>
Force all pixels above the threshold into white

```php
public whiteThresholdImage(mixed $threshold): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$threshold` | **mixed** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.whitethresholdimage.php - 

***

### appendImages

(PECL imagick 2.0.0)<br/>
Append a set of images

```php
public appendImages(bool $stack = false): \Imagick
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$stack` | **bool** | [optional] &lt;p&gt;<br />Whether to stack the images vertically.<br />By default (or if &lt;b&gt;FALSE&lt;/b&gt; is specified) images are stacked left-to-right.<br />If &lt;i&gt;stack&lt;/i&gt; is &lt;b&gt;TRUE&lt;/b&gt;, images are stacked top-to-bottom.<br />&lt;/p&gt; |


**Return Value:**

Imagick instance on success.




**See Also:**

* https://php.net/manual/en/imagick.appendimages.php - 

***

### charcoalImage

(PECL imagick 2.0.0)<br/>
Simulates a charcoal drawing

```php
public charcoalImage(float $radius, float $sigma): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** | &lt;p&gt;<br />The radius of the Gaussian, in pixels, not counting the center pixel<br />&lt;/p&gt; |
| `$sigma` | **float** | &lt;p&gt;<br />The standard deviation of the Gaussian, in pixels<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.charcoalimage.php - 

***

### normalizeImage

(PECL imagick 2.0.0)<br/>
Enhances the contrast of a color image

```php
public normalizeImage(int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.normalizeimage.php - 

***

### oilPaintImage

(PECL imagick 2.0.0)<br/>
Simulates an oil painting

```php
public oilPaintImage(float $radius): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** | &lt;p&gt;<br />The radius of the circular neighborhood.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.oilpaintimage.php - 

***

### posterizeImage

(PECL imagick 2.0.0)<br/>
Reduces the image to a limited number of color level

```php
public posterizeImage(int $levels, bool $dither): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$levels` | **int** |  |
| `$dither` | **bool** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.posterizeimage.php - 

***

### radialBlurImage

(PECL imagick 2.0.0)<br/>
Radial blurs an image

```php
public radialBlurImage(float $angle, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$angle` | **float** |  |
| `$channel` | **int** | [optional] |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.radialblurimage.php - 

***

### raiseImage

(PECL imagick 2.0.0)<br/>
Creates a simulated 3d button-like effect

```php
public raiseImage(int $width, int $height, int $x, int $y, bool $raise): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$width` | **int** |  |
| `$height` | **int** |  |
| `$x` | **int** |  |
| `$y` | **int** |  |
| `$raise` | **bool** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.raiseimage.php - 

***

### resampleImage

(PECL imagick 2.0.0)<br/>
Resample image to desired resolution

```php
public resampleImage(float $x_resolution, float $y_resolution, int $filter, float $blur): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x_resolution` | **float** |  |
| `$y_resolution` | **float** |  |
| `$filter` | **int** |  |
| `$blur` | **float** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.resampleimage.php - 

***

### resizeImage

Scales an image to the desired dimensions with one of these filters:<br>
If legacy is true, the calculations are done with the small rounding bug that existed in Imagick before 3.4.0.<br>
If false, the calculations should produce the same results as ImageMagick CLI does.<br>
<br>
<b>Note:</b> The behavior of the parameter bestfit changed in Imagick 3.0.0. Before this version given dimensions 400x400 an image of dimensions 200x150 would be left untouched.<br>
In Imagick 3.0.0 and later the image would be scaled up to size 400x300 as this is the "best fit" for the given dimensions. If bestfit parameter is used both width and height must be given.

```php
public resizeImage(int $columns, int $rows, int $filter, float $blur, bool $bestfit = false, bool $legacy = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$columns` | **int** | Width of the image |
| `$rows` | **int** | Height of the image |
| `$filter` | **int** | Refer to the list of filter constants. |
| `$blur` | **float** | The blur factor where &gt; 1 is blurry, &lt; 1 is sharp. |
| `$bestfit` | **bool** | [optional] Added since 2.1.0. Added optional fit parameter. This method now supports proportional scaling. Pass zero as either parameter for proportional scaling |
| `$legacy` | **bool** | [optional] Added since 3.4.0. Default value FALSE |


**Return Value:**

TRUE on success




**See Also:**

* https://php.net/manual/en/imagick.resizeimage.php - 

***

### rollImage

(PECL imagick 2.0.0)<br/>
Offsets an image

```php
public rollImage(int $x, int $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **int** | &lt;p&gt;<br />The X offset.<br />&lt;/p&gt; |
| `$y` | **int** | &lt;p&gt;<br />The Y offset.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.rollimage.php - 

***

### rotateImage

(PECL imagick 2.0.0)<br/>
Rotates an image

```php
public rotateImage(mixed $background, float $degrees): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$background` | **mixed** | &lt;p&gt;<br />The background color<br />&lt;/p&gt; |
| `$degrees` | **float** | &lt;p&gt;<br />The number of degrees to rotate the image<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.rotateimage.php - 

***

### sampleImage

(PECL imagick 2.0.0)<br/>
Scales an image with pixel sampling

```php
public sampleImage(int $columns, int $rows): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$columns` | **int** |  |
| `$rows` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.sampleimage.php - 

***

### solarizeImage

(PECL imagick 2.0.0)<br/>
Applies a solarizing effect to the image

```php
public solarizeImage(int $threshold): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$threshold` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.solarizeimage.php - 

***

### shadowImage

(PECL imagick 2.0.0)<br/>
Simulates an image shadow

```php
public shadowImage(float $opacity, float $sigma, int $x, int $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$opacity` | **float** |  |
| `$sigma` | **float** |  |
| `$x` | **int** |  |
| `$y` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.shadowimage.php - 

***

### setImageAttribute



```php
public setImageAttribute(mixed $key, mixed $value): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** |  |
| `$value` | **mixed** |  |





***

### setImageBackgroundColor

(PECL imagick 2.0.0)<br/>
Sets the image background color

```php
public setImageBackgroundColor(mixed $background): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$background` | **mixed** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagebackgroundcolor.php - 

***

### setImageCompose

(PECL imagick 2.0.0)<br/>
Sets the image composite operator

```php
public setImageCompose(int $compose): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compose` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagecompose.php - 

***

### setImageCompression

(PECL imagick 2.0.0)<br/>
Sets the image compression

```php
public setImageCompression(int $compression): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compression` | **int** | &lt;p&gt;<br />One of the &lt;b&gt;COMPRESSION&lt;/b&gt; constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagecompression.php - 

***

### setImageDelay

(PECL imagick 2.0.0)<br/>
Sets the image delay

```php
public setImageDelay(int $delay): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$delay` | **int** | &lt;p&gt;<br />The amount of time expressed in &#039;ticks&#039; that the image should be<br />displayed for. For animated GIFs there are 100 ticks per second, so a<br />value of 20 would be 20/100 of a second aka 1/5th of a second.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagedelay.php - 

***

### setImageDepth

(PECL imagick 2.0.0)<br/>
Sets the image depth

```php
public setImageDepth(int $depth): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$depth` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagedepth.php - 

***

### setImageGamma

(PECL imagick 2.0.0)<br/>
Sets the image gamma

```php
public setImageGamma(float $gamma): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$gamma` | **float** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagegamma.php - 

***

### setImageIterations

(PECL imagick 2.0.0)<br/>
Sets the image iterations

```php
public setImageIterations(int $iterations): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$iterations` | **int** | &lt;p&gt;<br />The number of iterations the image should loop over. Set to &#039;0&#039; to loop<br />continuously.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageiterations.php - 

***

### setImageMatteColor

(PECL imagick 2.0.0)<br/>
Sets the image matte color

```php
public setImageMatteColor(mixed $matte): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matte` | **mixed** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagemattecolor.php - 

***

### setImagePage

(PECL imagick 2.0.0)<br/>
Sets the page geometry of the image

```php
public setImagePage(int $width, int $height, int $x, int $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$width` | **int** |  |
| `$height` | **int** |  |
| `$x` | **int** |  |
| `$y` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagepage.php - 

***

### setImageProgressMonitor



```php
public setImageProgressMonitor(mixed $filename): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **mixed** |  |





***

### setImageResolution

(PECL imagick 2.0.0)<br/>
Sets the image resolution

```php
public setImageResolution(float $x_resolution, float $y_resolution): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x_resolution` | **float** |  |
| `$y_resolution` | **float** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageresolution.php - 

***

### setImageScene

(PECL imagick 2.0.0)<br/>
Sets the image scene

```php
public setImageScene(int $scene): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$scene` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagescene.php - 

***

### setImageTicksPerSecond

(PECL imagick 2.0.0)<br/>
Sets the image ticks-per-second

```php
public setImageTicksPerSecond(int $ticks_per_second): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ticks_per_second` | **int** | &lt;p&gt;<br />The duration for which an image should be displayed expressed in ticks<br />per second.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagetickspersecond.php - 

***

### setImageType

(PECL imagick 2.0.0)<br/>
Sets the image type

```php
public setImageType(int $image_type): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$image_type` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagetype.php - 

***

### setImageUnits

(PECL imagick 2.0.0)<br/>
Sets the image units of resolution

```php
public setImageUnits(int $units): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$units` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageunits.php - 

***

### sharpenImage

(PECL imagick 2.0.0)<br/>
Sharpens an image

```php
public sharpenImage(float $radius, float $sigma, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** |  |
| `$sigma` | **float** |  |
| `$channel` | **int** | [optional] |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.sharpenimage.php - 

***

### shaveImage

(PECL imagick 2.0.0)<br/>
Shaves pixels from the image edges

```php
public shaveImage(int $columns, int $rows): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$columns` | **int** |  |
| `$rows` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.shaveimage.php - 

***

### shearImage

(PECL imagick 2.0.0)<br/>
Creating a parallelogram

```php
public shearImage(mixed $background, float $x_shear, float $y_shear): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$background` | **mixed** | &lt;p&gt;<br />The background color<br />&lt;/p&gt; |
| `$x_shear` | **float** | &lt;p&gt;<br />The number of degrees to shear on the x axis<br />&lt;/p&gt; |
| `$y_shear` | **float** | &lt;p&gt;<br />The number of degrees to shear on the y axis<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.shearimage.php - 

***

### spliceImage

(PECL imagick 2.0.0)<br/>
Splices a solid color into the image

```php
public spliceImage(int $width, int $height, int $x, int $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$width` | **int** |  |
| `$height` | **int** |  |
| `$x` | **int** |  |
| `$y` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.spliceimage.php - 

***

### pingImage

(PECL imagick 2.0.0)<br/>
Fetch basic attributes about the image

```php
public pingImage(string $filename): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** | &lt;p&gt;<br />The filename to read the information from.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.pingimage.php - 

***

### readImageFile

(PECL imagick 2.0.0)<br/>
Reads image from open filehandle

```php
public readImageFile(resource $filehandle, string $fileName = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filehandle` | **resource** |  |
| `$fileName` | **string** | [optional] |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.readimagefile.php - 

***

### displayImage

(PECL imagick 2.0.0)<br/>
Displays an image

```php
public displayImage(string $servername): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$servername` | **string** | &lt;p&gt;<br />The X server name<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.displayimage.php - 

***

### displayImages

(PECL imagick 2.0.0)<br/>
Displays an image or image sequence

```php
public displayImages(string $servername): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$servername` | **string** | &lt;p&gt;<br />The X server name<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.displayimages.php - 

***

### spreadImage

(PECL imagick 2.0.0)<br/>
Randomly displaces each pixel in a block

```php
public spreadImage(float $radius): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.spreadimage.php - 

***

### swirlImage

(PECL imagick 2.0.0)<br/>
Swirls the pixels about the center of the image

```php
public swirlImage(float $degrees): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$degrees` | **float** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.swirlimage.php - 

***

### stripImage

(PECL imagick 2.0.0)<br/>
Strips an image of all profiles and comments

```php
public stripImage(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.stripimage.php - 

***

### queryFormats

(PECL imagick 2.0.0)<br/>
Returns formats supported by Imagick

```php
public static queryFormats(string $pattern = &quot;*&quot;): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pattern` | **string** | [optional] |


**Return Value:**

an array containing the formats supported by Imagick.




**See Also:**

* https://php.net/manual/en/imagick.queryformats.php - 

***

### queryFonts

(PECL imagick 2.0.0)<br/>
Returns the configured fonts

```php
public static queryFonts(string $pattern = &quot;*&quot;): array
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pattern` | **string** | [optional] &lt;p&gt;<br />The query pattern<br />&lt;/p&gt; |


**Return Value:**

an array containing the configured fonts.




**See Also:**

* https://php.net/manual/en/imagick.queryfonts.php - 

***

### queryFontMetrics

(PECL imagick 2.0.0)<br/>
Returns an array representing the font metrics

```php
public queryFontMetrics(\ImagickDraw $properties, string $text, bool $multiline = null): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$properties` | **\ImagickDraw** | &lt;p&gt;<br />ImagickDraw object containing font properties<br />&lt;/p&gt; |
| `$text` | **string** | &lt;p&gt;<br />The text<br />&lt;/p&gt; |
| `$multiline` | **bool** | [optional] &lt;p&gt;<br />Multiline parameter. If left empty it is autodetected<br />&lt;/p&gt; |


**Return Value:**

a multi-dimensional array representing the font metrics.




**See Also:**

* https://php.net/manual/en/imagick.queryfontmetrics.php - 

***

### steganoImage

(PECL imagick 2.0.0)<br/>
Hides a digital watermark within the image

```php
public steganoImage(\Imagick $watermark_wand, int $offset): \Imagick
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$watermark_wand` | **\Imagick** |  |
| `$offset` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.steganoimage.php - 

***

### addNoiseImage

(PECL imagick 2.0.0)<br/>
Adds random noise to the image

```php
public addNoiseImage(int $noise_type, int $channel = Imagick::CHANNEL_DEFAULT): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$noise_type` | **int** | &lt;p&gt;<br />The type of the noise. Refer to this list of<br />noise constants.<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To apply to more than one channel, combine channel constants using bitwise operators. Defaults to &lt;b&gt;Imagick::CHANNEL_DEFAULT&lt;/b&gt;. Refer to this list of channel constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.addnoiseimage.php - 

***

### motionBlurImage

(PECL imagick 2.0.0)<br/>
Simulates motion blur

```php
public motionBlurImage(float $radius, float $sigma, float $angle, int $channel = Imagick::CHANNEL_DEFAULT): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** | &lt;p&gt;<br />The radius of the Gaussian, in pixels, not counting the center pixel.<br />&lt;/p&gt; |
| `$sigma` | **float** | &lt;p&gt;<br />The standard deviation of the Gaussian, in pixels.<br />&lt;/p&gt; |
| `$angle` | **float** | &lt;p&gt;<br />Apply the effect along this angle.<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />The channel argument affects only if Imagick is compiled against ImageMagick version<br />6.4.4 or greater.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.motionblurimage.php - 

***

### mosaicImages

(PECL imagick 2.0.0)<br/>
Forms a mosaic from images

```php
public mosaicImages(): \Imagick
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.mosaicimages.php - 

***

### morphImages

(PECL imagick 2.0.0)<br/>
Method morphs a set of images

```php
public morphImages(int $number_frames): \Imagick
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$number_frames` | **int** | &lt;p&gt;<br />The number of in-between images to generate.<br />&lt;/p&gt; |


**Return Value:**

This method returns a new Imagick object on success.
Throw an <b>ImagickException</b> on error.



**Throws:**
<p>on error</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.morphimages.php - 

***

### minifyImage

(PECL imagick 2.0.0)<br/>
Scales an image proportionally to half its size

```php
public minifyImage(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.minifyimage.php - 

***

### affineTransformImage

(PECL imagick 2.0.0)<br/>
Transforms an image

```php
public affineTransformImage(\ImagickDraw $matrix): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matrix` | **\ImagickDraw** | &lt;p&gt;<br />The affine matrix<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.affinetransformimage.php - 

***

### averageImages

(PECL imagick 2.0.0)<br/>
Average a set of images

```php
public averageImages(): \Imagick
```









**Return Value:**

a new Imagick object on success.




**See Also:**

* https://php.net/manual/en/imagick.averageimages.php - 

***

### borderImage

(PECL imagick 2.0.0)<br/>
Surrounds the image with a border

```php
public borderImage(mixed $bordercolor, int $width, int $height): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bordercolor` | **mixed** | &lt;p&gt;<br />ImagickPixel object or a string containing the border color<br />&lt;/p&gt; |
| `$width` | **int** | &lt;p&gt;<br />Border width<br />&lt;/p&gt; |
| `$height` | **int** | &lt;p&gt;<br />Border height<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.borderimage.php - 

***

### chopImage

(PECL imagick 2.0.0)<br/>
Removes a region of an image and trims

```php
public chopImage(int $width, int $height, int $x, int $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$width` | **int** | &lt;p&gt;<br />Width of the chopped area<br />&lt;/p&gt; |
| `$height` | **int** | &lt;p&gt;<br />Height of the chopped area<br />&lt;/p&gt; |
| `$x` | **int** | &lt;p&gt;<br />X origo of the chopped area<br />&lt;/p&gt; |
| `$y` | **int** | &lt;p&gt;<br />Y origo of the chopped area<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.chopimage.php - 

***

### clipImage

(PECL imagick 2.0.0)<br/>
Clips along the first path from the 8BIM profile

```php
public clipImage(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.clipimage.php - 

***

### clipPathImage

(PECL imagick 2.0.0)<br/>
Clips along the named paths from the 8BIM profile

```php
public clipPathImage(string $pathname, bool $inside): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pathname` | **string** | &lt;p&gt;<br />The name of the path<br />&lt;/p&gt; |
| `$inside` | **bool** | &lt;p&gt;<br />If &lt;b&gt;TRUE&lt;/b&gt; later operations take effect inside clipping path.<br />Otherwise later operations take effect outside clipping path.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.clippathimage.php - 

***

### clipImagePath



```php
public clipImagePath(mixed $pathname, mixed $inside): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$pathname` | **mixed** |  |
| `$inside` | **mixed** |  |





***

### coalesceImages

(PECL imagick 2.0.0)<br/>
Composites a set of images

```php
public coalesceImages(): \Imagick
```









**Return Value:**

a new Imagick object on success.




**See Also:**

* https://php.net/manual/en/imagick.coalesceimages.php - 

***

### colorFloodfillImage

(PECL imagick 2.0.0)<br/>
Changes the color value of any pixel that matches target

```php
public colorFloodfillImage(mixed $fill, float $fuzz, mixed $bordercolor, int $x, int $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$fill` | **mixed** | &lt;p&gt;<br />ImagickPixel object containing the fill color<br />&lt;/p&gt; |
| `$fuzz` | **float** | &lt;p&gt;<br />The amount of fuzz. For example, set fuzz to 10 and the color red at<br />intensities of 100 and 102 respectively are now interpreted as the<br />same color for the purposes of the floodfill.<br />&lt;/p&gt; |
| `$bordercolor` | **mixed** | &lt;p&gt;<br />ImagickPixel object containing the border color<br />&lt;/p&gt; |
| `$x` | **int** | &lt;p&gt;<br />X start position of the floodfill<br />&lt;/p&gt; |
| `$y` | **int** | &lt;p&gt;<br />Y start position of the floodfill<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.colorfloodfillimage.php - 

***

### colorizeImage

Blends the fill color with each pixel in the image. The 'opacity' color is a per channel strength factor for how strongly the color should be applied.<br>
If legacy is true, the behaviour of this function is incorrect, but consistent with how it behaved before Imagick version 3.4.0

```php
public colorizeImage(mixed $colorize, mixed $opacity, bool $legacy = false): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$colorize` | **mixed** | &lt;p&gt;<br />ImagickPixel object or a string containing the colorize color<br />&lt;/p&gt; |
| `$opacity` | **mixed** | &lt;p&gt;<br />ImagickPixel object or an float containing the opacity value.<br />1.0 is fully opaque and 0.0 is fully transparent.<br />&lt;/p&gt; |
| `$legacy` | **bool** | [optional] Added since 3.4.0. Default value FALSE |


**Return Value:**

<b>TRUE</b> on success.



**Throws:**
<p>Throws ImagickException on error</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.colorizeimage.php - 

***

### compareImageChannels

(PECL imagick 2.0.0)<br/>
Returns the difference in one or more images

```php
public compareImageChannels(\Imagick $image, int $channelType, int $metricType): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$image` | **\Imagick** | &lt;p&gt;<br />Imagick object containing the image to compare.<br />&lt;/p&gt; |
| `$channelType` | **int** | &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |
| `$metricType` | **int** | &lt;p&gt;<br />One of the metric type constants.<br />&lt;/p&gt; |


**Return Value:**

Array consisting of new_wand and
distortion.




**See Also:**

* https://php.net/manual/en/imagick.compareimagechannels.php - 

***

### compareImages

(PECL imagick 2.0.0)<br/>
Compares an image to a reconstructed image

```php
public compareImages(\Imagick $compare, int $metric): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compare` | **\Imagick** | &lt;p&gt;<br />An image to compare to.<br />&lt;/p&gt; |
| `$metric` | **int** | &lt;p&gt;<br />Provide a valid metric type constant. Refer to this<br />list of metric constants.<br />&lt;/p&gt; |


**Return Value:**

Array consisting of an Imagick object of the
reconstructed image and a float representing the difference.



**Throws:**
<p>Throws ImagickException on error.</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.compareimages.php - 

***

### contrastImage

(PECL imagick 2.0.0)<br/>
Change the contrast of the image

```php
public contrastImage(bool $sharpen): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sharpen` | **bool** | &lt;p&gt;<br />The sharpen value<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.contrastimage.php - 

***

### combineImages

(PECL imagick 2.0.0)<br/>
Combines one or more images into a single image

```php
public combineImages(int $channelType): \Imagick
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channelType` | **int** | &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.combineimages.php - 

***

### convolveImage

(PECL imagick 2.0.0)<br/>
Applies a custom convolution kernel to the image

```php
public convolveImage(array $kernel, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$kernel` | **array** | &lt;p&gt;<br />The convolution kernel<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.convolveimage.php - 

***

### cycleColormapImage

(PECL imagick 2.0.0)<br/>
Displaces an image's colormap

```php
public cycleColormapImage(int $displace): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$displace` | **int** | &lt;p&gt;<br />The amount to displace the colormap.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.cyclecolormapimage.php - 

***

### deconstructImages

(PECL imagick 2.0.0)<br/>
Returns certain pixel differences between images

```php
public deconstructImages(): \Imagick
```









**Return Value:**

a new Imagick object on success.




**See Also:**

* https://php.net/manual/en/imagick.deconstructimages.php - 

***

### despeckleImage

(PECL imagick 2.0.0)<br/>
Reduces the speckle noise in an image

```php
public despeckleImage(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.despeckleimage.php - 

***

### edgeImage

(PECL imagick 2.0.0)<br/>
Enhance edges within the image

```php
public edgeImage(float $radius): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** | &lt;p&gt;<br />The radius of the operation.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.edgeimage.php - 

***

### embossImage

(PECL imagick 2.0.0)<br/>
Returns a grayscale image with a three-dimensional effect

```php
public embossImage(float $radius, float $sigma): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** | &lt;p&gt;<br />The radius of the effect<br />&lt;/p&gt; |
| `$sigma` | **float** | &lt;p&gt;<br />The sigma of the effect<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.embossimage.php - 

***

### enhanceImage

(PECL imagick 2.0.0)<br/>
Improves the quality of a noisy image

```php
public enhanceImage(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.enhanceimage.php - 

***

### equalizeImage

(PECL imagick 2.0.0)<br/>
Equalizes the image histogram

```php
public equalizeImage(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.equalizeimage.php - 

***

### evaluateImage

(PECL imagick 2.0.0)<br/>
Applies an expression to an image

```php
public evaluateImage(int $op, float $constant, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$op` | **int** | &lt;p&gt;<br />The evaluation operator<br />&lt;/p&gt; |
| `$constant` | **float** | &lt;p&gt;<br />The value of the operator<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.evaluateimage.php - 

***

### flattenImages

Merges a sequence of images. This is useful for combining Photoshop layers into a single image.

```php
public flattenImages(): \Imagick
```

This is replaced by:
<pre>
$im = $im->mergeImageLayers(\Imagick::LAYERMETHOD_FLATTEN)
</pre>







**Return Value:**

Returns an Imagick object containing the merged image.



**Throws:**
<p>Throws ImagickException on error.</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.flattenimages.php - 

***

### flipImage

(PECL imagick 2.0.0)<br/>
Creates a vertical mirror image

```php
public flipImage(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.flipimage.php - 

***

### flopImage

(PECL imagick 2.0.0)<br/>
Creates a horizontal mirror image

```php
public flopImage(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.flopimage.php - 

***

### frameImage

(PECL imagick 2.0.0)<br/>
Adds a simulated three-dimensional border

```php
public frameImage(mixed $matte_color, int $width, int $height, int $inner_bevel, int $outer_bevel): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$matte_color` | **mixed** | &lt;p&gt;<br />ImagickPixel object or a string representing the matte color<br />&lt;/p&gt; |
| `$width` | **int** | &lt;p&gt;<br />The width of the border<br />&lt;/p&gt; |
| `$height` | **int** | &lt;p&gt;<br />The height of the border<br />&lt;/p&gt; |
| `$inner_bevel` | **int** | &lt;p&gt;<br />The inner bevel width<br />&lt;/p&gt; |
| `$outer_bevel` | **int** | &lt;p&gt;<br />The outer bevel width<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.frameimage.php - 

***

### fxImage

(PECL imagick 2.0.0)<br/>
Evaluate expression for each pixel in the image

```php
public fxImage(string $expression, int $channel = Imagick::CHANNEL_ALL): \Imagick
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$expression` | **string** | &lt;p&gt;<br />The expression.<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.fximage.php - 

***

### gammaImage

(PECL imagick 2.0.0)<br/>
Gamma-corrects an image

```php
public gammaImage(float $gamma, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$gamma` | **float** | &lt;p&gt;<br />The amount of gamma-correction.<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.gammaimage.php - 

***

### gaussianBlurImage

(PECL imagick 2.0.0)<br/>
Blurs an image

```php
public gaussianBlurImage(float $radius, float $sigma, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** | &lt;p&gt;<br />The radius of the Gaussian, in pixels, not counting the center pixel.<br />&lt;/p&gt; |
| `$sigma` | **float** | &lt;p&gt;<br />The standard deviation of the Gaussian, in pixels.<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.gaussianblurimage.php - 

***

### getImageAttribute



```php
public getImageAttribute(mixed $key): mixed
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **mixed** |  |





***

### getImageBackgroundColor

(PECL imagick 2.0.0)<br/>
Returns the image background color

```php
public getImageBackgroundColor(): \ImagickPixel
```









**Return Value:**

an ImagickPixel set to the background color of the image.




**See Also:**

* https://php.net/manual/en/imagick.getimagebackgroundcolor.php - 

***

### getImageBluePrimary

(PECL imagick 2.0.0)<br/>
Returns the chromaticy blue primary point

```php
public getImageBluePrimary(): array
```









**Return Value:**

Array consisting of "x" and "y" coordinates of point.




**See Also:**

* https://php.net/manual/en/imagick.getimageblueprimary.php - 

***

### getImageBorderColor

(PECL imagick 2.0.0)<br/>
Returns the image border color

```php
public getImageBorderColor(): \ImagickPixel
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.getimagebordercolor.php - 

***

### getImageChannelDepth

(PECL imagick 2.0.0)<br/>
Gets the depth for a particular image channel

```php
public getImageChannelDepth(int $channel): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **int** | &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To apply to more than one channel, combine channel constants using bitwise operators. Defaults to &lt;b&gt;Imagick::CHANNEL_DEFAULT&lt;/b&gt;. Refer to this list of channel constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.getimagechanneldepth.php - 

***

### getImageChannelDistortion

(PECL imagick 2.0.0)<br/>
Compares image channels of an image to a reconstructed image

```php
public getImageChannelDistortion(\Imagick $reference, int $channel, int $metric): float
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reference` | **\Imagick** | &lt;p&gt;<br />Imagick object to compare to.<br />&lt;/p&gt; |
| `$channel` | **int** | &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |
| `$metric` | **int** | &lt;p&gt;<br />One of the metric type constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.getimagechanneldistortion.php - 

***

### getImageChannelExtrema

(PECL imagick 2.0.0)<br/>
Gets the extrema for one or more image channels

```php
public getImageChannelExtrema(int $channel): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **int** | &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.getimagechannelextrema.php - 

***

### getImageChannelMean

(PECL imagick 2.0.0)<br/>
Gets the mean and standard deviation

```php
public getImageChannelMean(int $channel): array
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **int** | &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.getimagechannelmean.php - 

***

### getImageChannelStatistics

(PECL imagick 2.0.0)<br/>
Returns statistics for each channel in the image

```php
public getImageChannelStatistics(): array
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.getimagechannelstatistics.php - 

***

### getImageColormapColor

(PECL imagick 2.0.0)<br/>
Returns the color of the specified colormap index

```php
public getImageColormapColor(int $index): \ImagickPixel
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **int** | &lt;p&gt;<br />The offset into the image colormap.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.getimagecolormapcolor.php - 

***

### getImageColorspace

(PECL imagick 2.0.0)<br/>
Gets the image colorspace

```php
public getImageColorspace(): int
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.getimagecolorspace.php - 

***

### getImageCompose

(PECL imagick 2.0.0)<br/>
Returns the composite operator associated with the image

```php
public getImageCompose(): int
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.getimagecompose.php - 

***

### getImageDelay

(PECL imagick 2.0.0)<br/>
Gets the image delay

```php
public getImageDelay(): int
```









**Return Value:**

the image delay.




**See Also:**

* https://php.net/manual/en/imagick.getimagedelay.php - 

***

### getImageDepth

(PECL imagick 0.9.1-0.9.9)<br/>
Gets the image depth

```php
public getImageDepth(): int
```









**Return Value:**

The image depth.




**See Also:**

* https://php.net/manual/en/imagick.getimagedepth.php - 

***

### getImageDistortion

(PECL imagick 2.0.0)<br/>
Compares an image to a reconstructed image

```php
public getImageDistortion(\Imagick $reference, int $metric): float
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$reference` | **\Imagick** | &lt;p&gt;<br />Imagick object to compare to.<br />&lt;/p&gt; |
| `$metric` | **int** | &lt;p&gt;<br />One of the metric type constants.<br />&lt;/p&gt; |


**Return Value:**

the distortion metric used on the image (or the best guess
thereof).




**See Also:**

* https://php.net/manual/en/imagick.getimagedistortion.php - 

***

### getImageExtrema

(PECL imagick 2.0.0)<br/>
Gets the extrema for the image

```php
public getImageExtrema(): array
```









**Return Value:**

an associative array with the keys "min" and "max".




**See Also:**

* https://php.net/manual/en/imagick.getimageextrema.php - 

***

### getImageDispose

(PECL imagick 2.0.0)<br/>
Gets the image disposal method

```php
public getImageDispose(): int
```









**Return Value:**

the dispose method on success.




**See Also:**

* https://php.net/manual/en/imagick.getimagedispose.php - 

***

### getImageGamma

(PECL imagick 2.0.0)<br/>
Gets the image gamma

```php
public getImageGamma(): float
```









**Return Value:**

the image gamma on success.




**See Also:**

* https://php.net/manual/en/imagick.getimagegamma.php - 

***

### getImageGreenPrimary

(PECL imagick 2.0.0)<br/>
Returns the chromaticy green primary point

```php
public getImageGreenPrimary(): array
```









**Return Value:**

an array with the keys "x" and "y" on success, throws an ImagickException on failure.



**Throws:**
<p>on failure</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.getimagegreenprimary.php - 

***

### getImageHeight

(PECL imagick 2.0.0)<br/>
Returns the image height

```php
public getImageHeight(): int
```









**Return Value:**

the image height in pixels.




**See Also:**

* https://php.net/manual/en/imagick.getimageheight.php - 

***

### getImageHistogram

(PECL imagick 2.0.0)<br/>
Gets the image histogram

```php
public getImageHistogram(): array
```









**Return Value:**

the image histogram as an array of ImagickPixel objects.




**See Also:**

* https://php.net/manual/en/imagick.getimagehistogram.php - 

***

### getImageInterlaceScheme

(PECL imagick 2.0.0)<br/>
Gets the image interlace scheme

```php
public getImageInterlaceScheme(): int
```









**Return Value:**

the interlace scheme as an integer on success.
Trhow an <b>ImagickException</b> on error.



**Throws:**
<p>on error</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.getimageinterlacescheme.php - 

***

### getImageIterations

(PECL imagick 2.0.0)<br/>
Gets the image iterations

```php
public getImageIterations(): int
```









**Return Value:**

the image iterations as an integer.




**See Also:**

* https://php.net/manual/en/imagick.getimageiterations.php - 

***

### getImageMatteColor

(PECL imagick 2.0.0)<br/>
Returns the image matte color

```php
public getImageMatteColor(): \ImagickPixel
```









**Return Value:**

ImagickPixel object on success.




**See Also:**

* https://php.net/manual/en/imagick.getimagemattecolor.php - 

***

### getImagePage

(PECL imagick 2.0.0)<br/>
Returns the page geometry

```php
public getImagePage(): array
```









**Return Value:**

the page geometry associated with the image in an array with the
keys "width", "height", "x", and "y".




**See Also:**

* https://php.net/manual/en/imagick.getimagepage.php - 

***

### getImagePixelColor

(PECL imagick 2.0.0)<br/>
Returns the color of the specified pixel

```php
public getImagePixelColor(int $x, int $y): \ImagickPixel
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **int** | &lt;p&gt;<br />The x-coordinate of the pixel<br />&lt;/p&gt; |
| `$y` | **int** | &lt;p&gt;<br />The y-coordinate of the pixel<br />&lt;/p&gt; |


**Return Value:**

an ImagickPixel instance for the color at the coordinates given.




**See Also:**

* https://php.net/manual/en/imagick.getimagepixelcolor.php - 

***

### getImageProfile

(PECL imagick 2.0.0)<br/>
Returns the named image profile

```php
public getImageProfile(string $name): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | &lt;p&gt;<br />The name of the profile to return.<br />&lt;/p&gt; |


**Return Value:**

a string containing the image profile.




**See Also:**

* https://php.net/manual/en/imagick.getimageprofile.php - 

***

### getImageRedPrimary

(PECL imagick 2.0.0)<br/>
Returns the chromaticity red primary point

```php
public getImageRedPrimary(): array
```









**Return Value:**

the chromaticity red primary point as an array with the keys "x"
and "y".
Throw an <b>ImagickException</b> on error.



**Throws:**
<p>on error</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.getimageredprimary.php - 

***

### getImageRenderingIntent

(PECL imagick 2.0.0)<br/>
Gets the image rendering intent

```php
public getImageRenderingIntent(): int
```









**Return Value:**

the image rendering intent.




**See Also:**

* https://php.net/manual/en/imagick.getimagerenderingintent.php - 

***

### getImageResolution

(PECL imagick 2.0.0)<br/>
Gets the image X and Y resolution

```php
public getImageResolution(): array
```









**Return Value:**

the resolution as an array.




**See Also:**

* https://php.net/manual/en/imagick.getimageresolution.php - 

***

### getImageScene

(PECL imagick 2.0.0)<br/>
Gets the image scene

```php
public getImageScene(): int
```









**Return Value:**

the image scene.




**See Also:**

* https://php.net/manual/en/imagick.getimagescene.php - 

***

### getImageSignature

(PECL imagick 2.0.0)<br/>
Generates an SHA-256 message digest

```php
public getImageSignature(): string
```









**Return Value:**

a string containing the SHA-256 hash of the file.




**See Also:**

* https://php.net/manual/en/imagick.getimagesignature.php - 

***

### getImageTicksPerSecond

(PECL imagick 2.0.0)<br/>
Gets the image ticks-per-second

```php
public getImageTicksPerSecond(): int
```









**Return Value:**

the image ticks-per-second.




**See Also:**

* https://php.net/manual/en/imagick.getimagetickspersecond.php - 

***

### getImageType

(PECL imagick 0.9.10-0.9.9)<br/>
Gets the potential image type

```php
public getImageType(): int
```









**Return Value:**

the potential image type.
<b>imagick::IMGTYPE_UNDEFINED</b>
<b>imagick::IMGTYPE_BILEVEL</b>
<b>imagick::IMGTYPE_GRAYSCALE</b>
<b>imagick::IMGTYPE_GRAYSCALEMATTE</b>
<b>imagick::IMGTYPE_PALETTE</b>
<b>imagick::IMGTYPE_PALETTEMATTE</b>
<b>imagick::IMGTYPE_TRUECOLOR</b>
<b>imagick::IMGTYPE_TRUECOLORMATTE</b>
<b>imagick::IMGTYPE_COLORSEPARATION</b>
<b>imagick::IMGTYPE_COLORSEPARATIONMATTE</b>
<b>imagick::IMGTYPE_OPTIMIZE</b>




**See Also:**

* https://php.net/manual/en/imagick.getimagetype.php - 

***

### getImageUnits

(PECL imagick 2.0.0)<br/>
Gets the image units of resolution

```php
public getImageUnits(): int
```









**Return Value:**

the image units of resolution.




**See Also:**

* https://php.net/manual/en/imagick.getimageunits.php - 

***

### getImageVirtualPixelMethod

(PECL imagick 2.0.0)<br/>
Returns the virtual pixel method

```php
public getImageVirtualPixelMethod(): int
```









**Return Value:**

the virtual pixel method on success.




**See Also:**

* https://php.net/manual/en/imagick.getimagevirtualpixelmethod.php - 

***

### getImageWhitePoint

(PECL imagick 2.0.0)<br/>
Returns the chromaticity white point

```php
public getImageWhitePoint(): array
```









**Return Value:**

the chromaticity white point as an associative array with the keys
"x" and "y".




**See Also:**

* https://php.net/manual/en/imagick.getimagewhitepoint.php - 

***

### getImageWidth

(PECL imagick 2.0.0)<br/>
Returns the image width

```php
public getImageWidth(): int
```









**Return Value:**

the image width.




**See Also:**

* https://php.net/manual/en/imagick.getimagewidth.php - 

***

### getNumberImages

(PECL imagick 2.0.0)<br/>
Returns the number of images in the object

```php
public getNumberImages(): int
```









**Return Value:**

the number of images associated with Imagick object.




**See Also:**

* https://php.net/manual/en/imagick.getnumberimages.php - 

***

### getImageTotalInkDensity

(PECL imagick 2.0.0)<br/>
Gets the image total ink density

```php
public getImageTotalInkDensity(): float
```









**Return Value:**

the image total ink density of the image.
Throw an <b>ImagickException</b> on error.



**Throws:**
<p>on error</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.getimagetotalinkdensity.php - 

***

### getImageRegion

(PECL imagick 2.0.0)<br/>
Extracts a region of the image

```php
public getImageRegion(int $width, int $height, int $x, int $y): \Imagick
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$width` | **int** | &lt;p&gt;<br />The width of the extracted region.<br />&lt;/p&gt; |
| `$height` | **int** | &lt;p&gt;<br />The height of the extracted region.<br />&lt;/p&gt; |
| `$x` | **int** | &lt;p&gt;<br />X-coordinate of the top-left corner of the extracted region.<br />&lt;/p&gt; |
| `$y` | **int** | &lt;p&gt;<br />Y-coordinate of the top-left corner of the extracted region.<br />&lt;/p&gt; |


**Return Value:**

Extracts a region of the image and returns it as a new wand.




**See Also:**

* https://php.net/manual/en/imagick.getimageregion.php - 

***

### implodeImage

(PECL imagick 2.0.0)<br/>
Creates a new image as a copy

```php
public implodeImage(float $radius): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** | &lt;p&gt;<br />The radius of the implode<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.implodeimage.php - 

***

### levelImage

(PECL imagick 2.0.0)<br/>
Adjusts the levels of an image

```php
public levelImage(float $blackPoint, float $gamma, float $whitePoint, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$blackPoint` | **float** | &lt;p&gt;<br />The image black point<br />&lt;/p&gt; |
| `$gamma` | **float** | &lt;p&gt;<br />The gamma value<br />&lt;/p&gt; |
| `$whitePoint` | **float** | &lt;p&gt;<br />The image white point<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.levelimage.php - 

***

### magnifyImage

(PECL imagick 2.0.0)<br/>
Scales an image proportionally 2x

```php
public magnifyImage(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.magnifyimage.php - 

***

### mapImage

(PECL imagick 2.0.0)<br/>
Replaces the colors of an image with the closest color from a reference image.

```php
public mapImage(\Imagick $map, bool $dither): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$map` | **\Imagick** |  |
| `$dither` | **bool** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.mapimage.php - 

***

### matteFloodfillImage

(PECL imagick 2.0.0)<br/>
Changes the transparency value of a color

```php
public matteFloodfillImage(float $alpha, float $fuzz, mixed $bordercolor, int $x, int $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$alpha` | **float** | &lt;p&gt;<br />The level of transparency: 1.0 is fully opaque and 0.0 is fully<br />transparent.<br />&lt;/p&gt; |
| `$fuzz` | **float** | &lt;p&gt;<br />The fuzz member of image defines how much tolerance is acceptable to<br />consider two colors as the same.<br />&lt;/p&gt; |
| `$bordercolor` | **mixed** | &lt;p&gt;<br />An &lt;b&gt;ImagickPixel&lt;/b&gt; object or string representing the border color.<br />&lt;/p&gt; |
| `$x` | **int** | &lt;p&gt;<br />The starting x coordinate of the operation.<br />&lt;/p&gt; |
| `$y` | **int** | &lt;p&gt;<br />The starting y coordinate of the operation.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.mattefloodfillimage.php - 

***

### medianFilterImage

(PECL imagick 2.0.0)<br/>
Applies a digital filter

```php
public medianFilterImage(float $radius): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** | &lt;p&gt;<br />The radius of the pixel neighborhood.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.medianfilterimage.php - 

***

### negateImage

(PECL imagick 2.0.0)<br/>
Negates the colors in the reference image

```php
public negateImage(bool $gray, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$gray` | **bool** | &lt;p&gt;<br />Whether to only negate grayscale pixels within the image.<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.negateimage.php - 

***

### paintOpaqueImage

(PECL imagick 2.0.0)<br/>
Change any pixel that matches color

```php
public paintOpaqueImage(mixed $target, mixed $fill, float $fuzz, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$target` | **mixed** | &lt;p&gt;<br />Change this target color to the fill color within the image. An<br />ImagickPixel object or a string representing the target color.<br />&lt;/p&gt; |
| `$fill` | **mixed** | &lt;p&gt;<br />An ImagickPixel object or a string representing the fill color.<br />&lt;/p&gt; |
| `$fuzz` | **float** | &lt;p&gt;<br />The fuzz member of image defines how much tolerance is acceptable to<br />consider two colors as the same.<br />&lt;/p&gt; |
| `$channel` | **int** | [optional] &lt;p&gt;<br />Provide any channel constant that is valid for your channel mode. To<br />apply to more than one channel, combine channeltype constants using<br />bitwise operators. Refer to this<br />list of channel constants.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.paintopaqueimage.php - 

***

### paintTransparentImage

(PECL imagick 2.0.0)<br/>
Changes any pixel that matches color with the color defined by fill

```php
public paintTransparentImage(mixed $target, float $alpha, float $fuzz): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$target` | **mixed** | &lt;p&gt;<br />Change this target color to specified opacity value within the image.<br />&lt;/p&gt; |
| `$alpha` | **float** | &lt;p&gt;<br />The level of transparency: 1.0 is fully opaque and 0.0 is fully<br />transparent.<br />&lt;/p&gt; |
| `$fuzz` | **float** | &lt;p&gt;<br />The fuzz member of image defines how much tolerance is acceptable to<br />consider two colors as the same.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.painttransparentimage.php - 

***

### previewImages

(PECL imagick 2.0.0)<br/>
Quickly pin-point appropriate parameters for image processing

```php
public previewImages(int $preview): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$preview` | **int** | &lt;p&gt;<br />Preview type. See Preview type constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.previewimages.php - 

***

### profileImage

(PECL imagick 2.0.0)<br/>
Adds or removes a profile from an image

```php
public profileImage(string $name, string $profile): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$profile` | **string** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.profileimage.php - 

***

### quantizeImage

(PECL imagick 2.0.0)<br/>
Analyzes the colors within a reference image

```php
public quantizeImage(int $numberColors, int $colorspace, int $treedepth, bool $dither, bool $measureError): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numberColors` | **int** |  |
| `$colorspace` | **int** |  |
| `$treedepth` | **int** |  |
| `$dither` | **bool** |  |
| `$measureError` | **bool** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.quantizeimage.php - 

***

### quantizeImages

(PECL imagick 2.0.0)<br/>
Analyzes the colors within a sequence of images

```php
public quantizeImages(int $numberColors, int $colorspace, int $treedepth, bool $dither, bool $measureError): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$numberColors` | **int** |  |
| `$colorspace` | **int** |  |
| `$treedepth` | **int** |  |
| `$dither` | **bool** |  |
| `$measureError` | **bool** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.quantizeimages.php - 

***

### reduceNoiseImage

(PECL imagick 2.0.0)<br/>
Smooths the contours of an image

```php
public reduceNoiseImage(float $radius): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.reducenoiseimage.php - 

***

### removeImageProfile

(PECL imagick 2.0.0)<br/>
Removes the named image profile and returns it

```php
public removeImageProfile(string $name): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |


**Return Value:**

a string containing the profile of the image.




**See Also:**

* https://php.net/manual/en/imagick.removeimageprofile.php - 

***

### separateImageChannel

(PECL imagick 2.0.0)<br/>
Separates a channel from the image

```php
public separateImageChannel(int $channel): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.separateimagechannel.php - 

***

### sepiaToneImage

(PECL imagick 2.0.0)<br/>
Sepia tones an image

```php
public sepiaToneImage(float $threshold): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$threshold` | **float** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.sepiatoneimage.php - 

***

### setImageBias

(PECL imagick 2.0.0)<br/>
Sets the image bias for any method that convolves an image

```php
public setImageBias(float $bias): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bias` | **float** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagebias.php - 

***

### setImageBluePrimary

(PECL imagick 2.0.0)<br/>
Sets the image chromaticity blue primary point

```php
public setImageBluePrimary(float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** |  |
| `$y` | **float** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageblueprimary.php - 

***

### setImageBorderColor

(PECL imagick 2.0.0)<br/>
Sets the image border color

```php
public setImageBorderColor(mixed $border): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$border` | **mixed** | &lt;p&gt;<br />The border color<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagebordercolor.php - 

***

### setImageChannelDepth

(PECL imagick 2.0.0)<br/>
Sets the depth of a particular image channel

```php
public setImageChannelDepth(int $channel, int $depth): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **int** |  |
| `$depth` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagechanneldepth.php - 

***

### setImageColormapColor

(PECL imagick 2.0.0)<br/>
Sets the color of the specified colormap index

```php
public setImageColormapColor(int $index, \ImagickPixel $color): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$index` | **int** |  |
| `$color` | **\ImagickPixel** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagecolormapcolor.php - 

***

### setImageColorspace

(PECL imagick 2.0.0)<br/>
Sets the image colorspace

```php
public setImageColorspace(int $colorspace): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$colorspace` | **int** | &lt;p&gt;<br />One of the COLORSPACE constants<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagecolorspace.php - 

***

### setImageDispose

(PECL imagick 2.0.0)<br/>
Sets the image disposal method

```php
public setImageDispose(int $dispose): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$dispose` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagedispose.php - 

***

### setImageExtent

(PECL imagick 2.0.0)<br/>
Sets the image size

```php
public setImageExtent(int $columns, int $rows): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$columns` | **int** |  |
| `$rows` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageextent.php - 

***

### setImageGreenPrimary

(PECL imagick 2.0.0)<br/>
Sets the image chromaticity green primary point

```php
public setImageGreenPrimary(float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** |  |
| `$y` | **float** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagegreenprimary.php - 

***

### setImageInterlaceScheme

(PECL imagick 2.0.0)<br/>
Sets the image compression

```php
public setImageInterlaceScheme(int $interlace_scheme): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$interlace_scheme` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageinterlacescheme.php - 

***

### setImageProfile

(PECL imagick 2.0.0)<br/>
Adds a named profile to the Imagick object

```php
public setImageProfile(string $name, string $profile): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** |  |
| `$profile` | **string** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageprofile.php - 

***

### setImageRedPrimary

(PECL imagick 2.0.0)<br/>
Sets the image chromaticity red primary point

```php
public setImageRedPrimary(float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** |  |
| `$y` | **float** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimageredprimary.php - 

***

### setImageRenderingIntent

(PECL imagick 2.0.0)<br/>
Sets the image rendering intent

```php
public setImageRenderingIntent(int $rendering_intent): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$rendering_intent` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagerenderingintent.php - 

***

### setImageVirtualPixelMethod

(PECL imagick 2.0.0)<br/>
Sets the image virtual pixel method

```php
public setImageVirtualPixelMethod(int $method): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$method` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagevirtualpixelmethod.php - 

***

### setImageWhitePoint

(PECL imagick 2.0.0)<br/>
Sets the image chromaticity white point

```php
public setImageWhitePoint(float $x, float $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x` | **float** |  |
| `$y` | **float** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimagewhitepoint.php - 

***

### sigmoidalContrastImage

(PECL imagick 2.0.0)<br/>
Adjusts the contrast of an image

```php
public sigmoidalContrastImage(bool $sharpen, float $alpha, float $beta, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$sharpen` | **bool** |  |
| `$alpha` | **float** |  |
| `$beta` | **float** |  |
| `$channel` | **int** | [optional] |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.sigmoidalcontrastimage.php - 

***

### stereoImage

(PECL imagick 2.0.0)<br/>
Composites two images

```php
public stereoImage(\Imagick $offset_wand): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$offset_wand` | **\Imagick** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.stereoimage.php - 

***

### textureImage

(PECL imagick 2.0.0)<br/>
Repeatedly tiles the texture image

```php
public textureImage(\Imagick $texture_wand): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$texture_wand` | **\Imagick** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.textureimage.php - 

***

### tintImage

pplies a color vector to each pixel in the image. The 'opacity' color is a per channel strength factor for how strongly the color should be applied.

```php
public tintImage(mixed $tint, mixed $opacity, bool $legacy = false): bool
```

If legacy is true, the behaviour of this function is incorrect, but consistent with how it behaved before Imagick version 3.4.0






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$tint` | **mixed** |  |
| `$opacity` | **mixed** |  |
| `$legacy` | **bool** | [optional] |


**Return Value:**

<b>TRUE</b> on success.



**Throws:**
<p>Throws ImagickException on error</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.tintimage.php - 

***

### unsharpMaskImage

(PECL imagick 2.0.0)<br/>
Sharpens an image

```php
public unsharpMaskImage(float $radius, float $sigma, float $amount, float $threshold, int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** |  |
| `$sigma` | **float** |  |
| `$amount` | **float** |  |
| `$threshold` | **float** |  |
| `$channel` | **int** | [optional] |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.unsharpmaskimage.php - 

***

### getImage

(PECL imagick 2.0.0)<br/>
Returns a new Imagick object

```php
public getImage(): \Imagick
```









**Return Value:**

a new Imagick object with the current image sequence.




**See Also:**

* https://php.net/manual/en/imagick.getimage.php - 

***

### addImage

(PECL imagick 2.0.0)<br/>
Adds new image to Imagick object image list

```php
public addImage(\Imagick $source): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$source` | **\Imagick** | &lt;p&gt;<br />The source Imagick object<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.addimage.php - 

***

### setImage

(PECL imagick 2.0.0)<br/>
Replaces image in the object

```php
public setImage(\Imagick $replace): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$replace` | **\Imagick** | &lt;p&gt;<br />The replace Imagick object<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setimage.php - 

***

### newImage

(PECL imagick 2.0.0)<br/>
Creates a new image

```php
public newImage(int $cols, int $rows, mixed $background, string $format = null): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$cols` | **int** | &lt;p&gt;<br />Columns in the new image<br />&lt;/p&gt; |
| `$rows` | **int** | &lt;p&gt;<br />Rows in the new image<br />&lt;/p&gt; |
| `$background` | **mixed** | &lt;p&gt;<br />The background color used for this image<br />&lt;/p&gt; |
| `$format` | **string** | [optional] &lt;p&gt;<br />Image format. This parameter was added in Imagick version 2.0.1.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.newimage.php - 

***

### newPseudoImage

(PECL imagick 2.0.0)<br/>
Creates a new image

```php
public newPseudoImage(int $columns, int $rows, string $pseudoString): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$columns` | **int** | &lt;p&gt;<br />columns in the new image<br />&lt;/p&gt; |
| `$rows` | **int** | &lt;p&gt;<br />rows in the new image<br />&lt;/p&gt; |
| `$pseudoString` | **string** | &lt;p&gt;<br />string containing pseudo image definition.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.newpseudoimage.php - 

***

### getCompression

(PECL imagick 2.0.0)<br/>
Gets the object compression type

```php
public getCompression(): int
```









**Return Value:**

the compression constant




**See Also:**

* https://php.net/manual/en/imagick.getcompression.php - 

***

### getCompressionQuality

(PECL imagick 2.0.0)<br/>
Gets the object compression quality

```php
public getCompressionQuality(): int
```









**Return Value:**

integer describing the compression quality




**See Also:**

* https://php.net/manual/en/imagick.getcompressionquality.php - 

***

### getCopyright

(PECL imagick 2.0.0)<br/>
Returns the ImageMagick API copyright as a string

```php
public static getCopyright(): string
```



* This method is **static**.





**Return Value:**

a string containing the copyright notice of Imagemagick and
Magickwand C API.




**See Also:**

* https://php.net/manual/en/imagick.getcopyright.php - 

***

### getFilename

(PECL imagick 2.0.0)<br/>
The filename associated with an image sequence

```php
public getFilename(): string
```









**Return Value:**

a string on success.




**See Also:**

* https://php.net/manual/en/imagick.getfilename.php - 

***

### getFormat

(PECL imagick 2.0.0)<br/>
Returns the format of the Imagick object

```php
public getFormat(): string
```









**Return Value:**

the format of the image.




**See Also:**

* https://php.net/manual/en/imagick.getformat.php - 

***

### getHomeURL

(PECL imagick 2.0.0)<br/>
Returns the ImageMagick home URL

```php
public static getHomeURL(): string
```



* This method is **static**.





**Return Value:**

a link to the imagemagick homepage.




**See Also:**

* https://php.net/manual/en/imagick.gethomeurl.php - 

***

### getInterlaceScheme

(PECL imagick 2.0.0)<br/>
Gets the object interlace scheme

```php
public getInterlaceScheme(): int
```









**Return Value:**

Gets the wand interlace
scheme.




**See Also:**

* https://php.net/manual/en/imagick.getinterlacescheme.php - 

***

### getOption

(PECL imagick 2.0.0)<br/>
Returns a value associated with the specified key

```php
public getOption(string $key): string
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** | &lt;p&gt;<br />The name of the option<br />&lt;/p&gt; |


**Return Value:**

a value associated with a wand and the specified key.




**See Also:**

* https://php.net/manual/en/imagick.getoption.php - 

***

### getPackageName

(PECL imagick 2.0.0)<br/>
Returns the ImageMagick package name

```php
public static getPackageName(): string
```



* This method is **static**.





**Return Value:**

the ImageMagick package name as a string.




**See Also:**

* https://php.net/manual/en/imagick.getpackagename.php - 

***

### getPage

(PECL imagick 2.0.0)<br/>
Returns the page geometry

```php
public getPage(): array
```









**Return Value:**

the page geometry associated with the Imagick object in
an associative array with the keys "width", "height", "x", and "y",
throwing ImagickException on error.



**Throws:**
<p>on error</p>

- [`ImagickException`](./ImagickException.md)



**See Also:**

* https://php.net/manual/en/imagick.getpage.php - 

***

### getQuantumDepth

(PECL imagick 2.0.0)<br/>
Gets the quantum depth

```php
public static getQuantumDepth(): array
```



* This method is **static**.





**Return Value:**

the Imagick quantum depth as a string.




**See Also:**

* https://php.net/manual/en/imagick.getquantumdepth.php - 

***

### getQuantumRange

(PECL imagick 2.0.0)<br/>
Returns the Imagick quantum range

```php
public static getQuantumRange(): array
```



* This method is **static**.





**Return Value:**

the Imagick quantum range as a string.




**See Also:**

* https://php.net/manual/en/imagick.getquantumrange.php - 

***

### getReleaseDate

(PECL imagick 2.0.0)<br/>
Returns the ImageMagick release date

```php
public static getReleaseDate(): string
```



* This method is **static**.





**Return Value:**

the ImageMagick release date as a string.




**See Also:**

* https://php.net/manual/en/imagick.getreleasedate.php - 

***

### getResource

(PECL imagick 2.0.0)<br/>
Returns the specified resource's memory usage

```php
public static getResource(int $type): int
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **int** | &lt;p&gt;<br />Refer to the list of resourcetype constants.<br />&lt;/p&gt; |


**Return Value:**

the specified resource's memory usage in megabytes.




**See Also:**

* https://php.net/manual/en/imagick.getresource.php - 

***

### getResourceLimit

(PECL imagick 2.0.0)<br/>
Returns the specified resource limit

```php
public static getResourceLimit(int $type): int
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **int** | &lt;p&gt;<br />Refer to the list of resourcetype constants.<br />&lt;/p&gt; |


**Return Value:**

the specified resource limit in megabytes.




**See Also:**

* https://php.net/manual/en/imagick.getresourcelimit.php - 

***

### getSamplingFactors

(PECL imagick 2.0.0)<br/>
Gets the horizontal and vertical sampling factor

```php
public getSamplingFactors(): array
```









**Return Value:**

an associative array with the horizontal and vertical sampling
factors of the image.




**See Also:**

* https://php.net/manual/en/imagick.getsamplingfactors.php - 

***

### getSize

(PECL imagick 2.0.0)<br/>
Returns the size associated with the Imagick object

```php
public getSize(): array
```









**Return Value:**

the size associated with the Imagick object as an array with the
keys "columns" and "rows".




**See Also:**

* https://php.net/manual/en/imagick.getsize.php - 

***

### getVersion

(PECL imagick 2.0.0)<br/>
Returns the ImageMagick API version

```php
public static getVersion(): array
```



* This method is **static**.





**Return Value:**

the ImageMagick API version as a string and as a number.




**See Also:**

* https://php.net/manual/en/imagick.getversion.php - 

***

### setBackgroundColor

(PECL imagick 2.0.0)<br/>
Sets the object's default background color

```php
public setBackgroundColor(mixed $background): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$background` | **mixed** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setbackgroundcolor.php - 

***

### setCompression

(PECL imagick 2.0.0)<br/>
Sets the object's default compression type

```php
public setCompression(int $compression): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$compression` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setcompression.php - 

***

### setCompressionQuality

(PECL imagick 0.9.10-0.9.9)<br/>
Sets the object's default compression quality

```php
public setCompressionQuality(int $quality): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$quality` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setcompressionquality.php - 

***

### setFilename

(PECL imagick 2.0.0)<br/>
Sets the filename before you read or write the image

```php
public setFilename(string $filename): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$filename` | **string** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setfilename.php - 

***

### setFormat

(PECL imagick 2.0.0)<br/>
Sets the format of the Imagick object

```php
public setFormat(string $format): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$format` | **string** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setformat.php - 

***

### setInterlaceScheme

(PECL imagick 2.0.0)<br/>
Sets the image compression

```php
public setInterlaceScheme(int $interlace_scheme): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$interlace_scheme` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setinterlacescheme.php - 

***

### setOption

(PECL imagick 2.0.0)<br/>
Set an option

```php
public setOption(string $key, string $value): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** |  |
| `$value` | **string** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setoption.php - 

***

### setPage

(PECL imagick 2.0.0)<br/>
Sets the page geometry of the Imagick object

```php
public setPage(int $width, int $height, int $x, int $y): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$width` | **int** |  |
| `$height` | **int** |  |
| `$x` | **int** |  |
| `$y` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setpage.php - 

***

### setResourceLimit

(PECL imagick 2.0.0)<br/>
Sets the limit for a particular resource in megabytes

```php
public static setResourceLimit(int $type, int $limit): bool
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **int** | &lt;p&gt;<br />Refer to the list of resourcetype constants.<br />&lt;/p&gt; |
| `$limit` | **int** | &lt;p&gt;<br />The resource limit. The unit depends on the type of the resource being limited.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setresourcelimit.php - 

***

### setResolution

(PECL imagick 2.0.0)<br/>
Sets the image resolution

```php
public setResolution(float $x_resolution, float $y_resolution): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$x_resolution` | **float** | &lt;p&gt;<br />The horizontal resolution.<br />&lt;/p&gt; |
| `$y_resolution` | **float** | &lt;p&gt;<br />The vertical resolution.<br />&lt;/p&gt; |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setresolution.php - 

***

### setSamplingFactors

(PECL imagick 2.0.0)<br/>
Sets the image sampling factors

```php
public setSamplingFactors(array $factors): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$factors` | **array** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setsamplingfactors.php - 

***

### setSize

(PECL imagick 2.0.0)<br/>
Sets the size of the Imagick object

```php
public setSize(int $columns, int $rows): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$columns` | **int** |  |
| `$rows` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.setsize.php - 

***

### setType

(PECL imagick 2.0.0)<br/>
Sets the image type attribute

```php
public setType(int $image_type): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$image_type` | **int** |  |


**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.settype.php - 

***

### key



```php
public key(): mixed
```












***

### next



```php
public next(): mixed
```












***

### rewind



```php
public rewind(): mixed
```












***

### valid

(PECL imagick 2.0.0)<br/>
Checks if the current item is valid

```php
public valid(): bool
```









**Return Value:**

<b>TRUE</b> on success.




**See Also:**

* https://php.net/manual/en/imagick.valid.php - 

***

### current

(PECL imagick 2.0.0)<br/>
Returns a reference to the current Imagick object

```php
public current(): \Imagick
```









**Return Value:**

self on success.




**See Also:**

* https://php.net/manual/en/imagick.current.php - 

***

### brightnessContrastImage

Change the brightness and/or contrast of an image. It converts the brightness and contrast parameters into slope and intercept and calls a polynomical function to apply to the image.

```php
public brightnessContrastImage(string $brightness, string $contrast, int $CHANNEL = Imagick::CHANNEL_DEFAULT): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$brightness` | **string** |  |
| `$contrast` | **string** |  |
| `$CHANNEL` | **int** | [optional] |





**See Also:**

* https://php.net/manual/en/imagick.brightnesscontrastimage.php - 

***

### morphology

Applies a user supplied kernel to the image according to the given morphology method.

```php
public morphology(int $morphologyMethod, int $iterations, \ImagickKernel $ImagickKernel, int $CHANNEL = Imagick::CHANNEL_DEFAULT): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$morphologyMethod` | **int** | Which morphology method to use one of the \Imagick::MORPHOLOGY_* constants. |
| `$iterations` | **int** | The number of iteration to apply the morphology function. A value of -1 means loop until no change found. How this is applied may depend on the morphology method. Typically this is a value of 1. |
| `$ImagickKernel` | **\ImagickKernel** |  |
| `$CHANNEL` | **int** | [optional] |





**See Also:**

* https://php.net/manual/en/imagick.morphology.php - 

***

### filter

Applies a custom convolution kernel to the image.

```php
public filter(\ImagickKernel $ImagickKernel, int $CHANNEL = Imagick::CHANNEL_DEFAULT): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$ImagickKernel` | **\ImagickKernel** | An instance of ImagickKernel that represents either a single kernel or a linked series of kernels. |
| `$CHANNEL` | **int** | [optional] Provide any channel constant that is valid for your channel mode. To apply to more than one channel, combine channel constants using bitwise operators. Defaults to Imagick::CHANNEL_DEFAULT. Refer to this list of channel constants |





**See Also:**

* https://php.net/manual/en/imagick.filter.php - 

***

### colorMatrixImage

Apply color transformation to an image. The method permits saturation changes, hue rotation, luminance to alpha, and various other effects. Although variable-sized transformation matrices can be used, typically one uses a 5x5 matrix for an RGBA image and a 6x6 for CMYKA (or RGBA with offsets).

```php
public colorMatrixImage(string $color_matrix = Imagick::CHANNEL_DEFAULT): void
```

The matrix is similar to those used by Adobe Flash except offsets are in column 6 rather than 5 (in support of CMYKA images) and offsets are normalized (divide Flash offset by 255)






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$color_matrix` | **string** |  |





**See Also:**

* https://php.net/manual/en/imagick.colormatriximage.php - 

***

### deleteImageProperty

Deletes an image property.

```php
public deleteImageProperty(string $name): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$name` | **string** | The name of the property to delete. |





**See Also:**

* https://php.net/manual/en/imagick.deleteimageproperty.php - 

***

### forwardFourierTransformimage

Implements the discrete Fourier transform (DFT) of the image either as a magnitude / phase or real / imaginary image pair.

```php
public forwardFourierTransformimage(bool $magnitude): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$magnitude` | **bool** | If true, return as magnitude / phase pair otherwise a real / imaginary image pair. |





**See Also:**

* https://php.net/manual/en/imagick.forwardfouriertransformimage.php - 

***

### getImageCompression

Gets the current image's compression type.

```php
public getImageCompression(): int
```












**See Also:**

* https://php.net/manual/en/imagick.getimagecompression.php - 

***

### getRegistry

Get the StringRegistry entry for the named key or false if not set.

```php
public static getRegistry(string $key): string|false
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** |  |




**Throws:**
<p>Since version &gt;=3.4.3. Throws an exception if the key does not exist, rather than terminating the program.</p>

- [`Exception`](./Exception.md)



**See Also:**

* https://php.net/manual/en/imagick.getregistry.php - 

***

### getQuantum

Returns the ImageMagick quantum range as an integer.

```php
public static getQuantum(): int
```



* This method is **static**.








**See Also:**

* https://php.net/manual/en/imagick.getquantum.php - 

***

### identifyFormat

Replaces any embedded formatting characters with the appropriate image property and returns the interpreted text. See https://www.imagemagick.org/script/escape.php for escape sequences.

```php
public identifyFormat(string $embedText): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$embedText` | **string** | A string containing formatting sequences e.g. &quot;Trim box: %@ number of unique colors: %k&quot;. |





**See Also:**

* https://www.imagemagick.org/script/escape.php - * https://php.net/manual/en/imagick.identifyformat.php - 

***

### inverseFourierTransformImage

Implements the inverse discrete Fourier transform (DFT) of the image either as a magnitude / phase or real / imaginary image pair.

```php
public inverseFourierTransformImage(\Imagick $complement, bool $magnitude): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$complement` | **\Imagick** | The second image to combine with this one to form either the magnitude / phase or real / imaginary image pair. |
| `$magnitude` | **bool** | If true, combine as magnitude / phase pair otherwise a real / imaginary image pair. |





**See Also:**

* https://php.net/manual/en/imagick.inversefouriertransformimage.php - 

***

### listRegistry

List all the registry settings. Returns an array of all the key/value pairs in the registry

```php
public static listRegistry(): array
```



* This method is **static**.





**Return Value:**

An array containing the key/values from the registry.




**See Also:**

* https://php.net/manual/en/imagick.listregistry.php - 

***

### rotationalBlurImage

Rotational blurs an image.

```php
public rotationalBlurImage(string $angle, string $CHANNEL = Imagick::CHANNEL_DEFAULT): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$angle` | **string** |  |
| `$CHANNEL` | **string** |  |





**See Also:**

* https://php.net/manual/en/imagick.rotationalblurimage.php - 

***

### selectiveBlurImage

Selectively blur an image within a contrast threshold. It is similar to the unsharpen mask that sharpens everything with contrast above a certain threshold.

```php
public selectiveBlurImage(float $radius, float $sigma, float $threshold, int $CHANNEL = Imagick::CHANNEL_DEFAULT): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** |  |
| `$sigma` | **float** |  |
| `$threshold` | **float** |  |
| `$CHANNEL` | **int** | Provide any channel constant that is valid for your channel mode. To apply to more than one channel, combine channel constants using bitwise operators. Defaults to Imagick::CHANNEL_DEFAULT. Refer to this list of channel constants |





**See Also:**

* https://php.net/manual/en/imagick.selectiveblurimage.php - 

***

### setAntiAlias

Set whether antialiasing should be used for operations. On by default.

```php
public setAntiAlias(bool $antialias): int
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$antialias` | **bool** |  |





***

### setImageBiasQuantum



```php
public setImageBiasQuantum(string $bias): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$bias` | **string** |  |





**See Also:**

* https://php.net/manual/en/imagick.setimagebiasquantum.php - 

***

### setProgressMonitor

Set a callback that will be called during the processing of the Imagick image.

```php
public setProgressMonitor(callable $callback): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$callback` | **callable** | The progress function to call. It should return true if image processing should continue, or false if it should be cancelled.<br />The offset parameter indicates the progress and the span parameter indicates the total amount of work needed to be done.<br />&lt;pre&gt; bool callback ( mixed $offset , mixed $span ) &lt;/pre&gt;<br />&lt;b&gt;Caution&lt;/b&gt;<br />The values passed to the callback function are not consistent. In particular the span parameter can increase during image processing. Because of this calculating the percentage complete of an image operation is not trivial. |





**See Also:**

* https://php.net/manual/en/imagick.setprogressmonitor.php - 

***

### setRegistry

Sets the ImageMagick registry entry named key to value. This is most useful for setting "temporary-path" which controls where ImageMagick creates temporary images e.g. while processing PDFs.

```php
public static setRegistry(string $key, string $value): void
```



* This method is **static**.




**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$key` | **string** |  |
| `$value` | **string** |  |





**See Also:**

* https://php.net/manual/en/imagick.setregistry.php - 

***

### statisticImage

Replace each pixel with corresponding statistic from the neighborhood of the specified width and height.

```php
public statisticImage(int $type, int $width, int $height, int $channel = Imagick::CHANNEL_DEFAULT): void
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$type` | **int** |  |
| `$width` | **int** |  |
| `$height` | **int** |  |
| `$channel` | **int** | [optional] |





**See Also:**

* https://php.net/manual/en/imagick.statisticimage.php - 

***

### subImageMatch

Searches for a subimage in the current image and returns a similarity image such that an exact match location is
completely white and if none of the pixels match, black, otherwise some gray level in-between.

```php
public subImageMatch(\Imagick $imagick, array& $bestMatch, float& $similarity, float $similarity_threshold, int $metric): \Imagick
```

You can also pass in the optional parameters bestMatch and similarity. After calling the function similarity will
be set to the 'score' of the similarity between the subimage and the matching position in the larger image,
bestMatch will contain an associative array with elements x, y, width, height that describe the matching region.






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$imagick` | **\Imagick** |  |
| `$bestMatch` | **array** | [optional] |
| `$similarity` | **float** | [optional] A new image that displays the amount of similarity at each pixel. |
| `$similarity_threshold` | **float** | [optional] Only used if compiled with ImageMagick (library) &gt; 7 |
| `$metric` | **int** | [optional] Only used if compiled with ImageMagick (library) &gt; 7 |





**See Also:**

* https://php.net/manual/en/imagick.subimagematch.php - 

***

### similarityImage

Is an alias of Imagick::subImageMatch

```php
public similarityImage(\Imagick $imagick, array& $bestMatch, float& $similarity, float $similarity_threshold, int $metric): \Imagick
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$imagick` | **\Imagick** |  |
| `$bestMatch` | **array** | [optional] |
| `$similarity` | **float** | [optional] A new image that displays the amount of similarity at each pixel. |
| `$similarity_threshold` | **float** | [optional] |
| `$metric` | **int** | [optional] |





**See Also:**

* \Imagick::subImageMatch() - This function is an alias of subImageMatch()

***

### getConfigureOptions

Returns any ImageMagick  configure options that match the specified pattern (e.g. "*" for all). Options include NAME, VERSION, LIB_VERSION, etc.

```php
public getConfigureOptions(): string
```












***

### getFeatures

GetFeatures() returns the ImageMagick features that have been compiled into the runtime.

```php
public getFeatures(): string
```












***

### getHDRIEnabled



```php
public getHDRIEnabled(): int
```












***

### setImageChannelMask

Sets the image channel mask. Returns the previous set channel mask.

```php
public setImageChannelMask(int $channel): mixed
```

Only works with Imagick >=7






**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **int** |  |





***

### evaluateImages

Merge multiple images of the same size together with the selected operator. https://www.imagemagick.org/Usage/layers/#evaluate-sequence

```php
public evaluateImages(int $EVALUATE_CONSTANT): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$EVALUATE_CONSTANT` | **int** |  |





**See Also:**

* https://www.imagemagick.org/Usage/layers/#evaluate-sequence - 

***

### autoGammaImage

Extracts the 'mean' from the image and adjust the image to try make set its gamma appropriately.

```php
public autoGammaImage(int $channel = Imagick::CHANNEL_ALL): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$channel` | **int** | [optional] Default value Imagick::CHANNEL_ALL |





***

### autoOrient

Adjusts an image so that its orientation is suitable $ for viewing (i.e. top-left orientation).

```php
public autoOrient(): bool
```












***

### compositeImageGravity

Composite one image onto another using the specified gravity.

```php
public compositeImageGravity(\Imagick $imagick, int $COMPOSITE_CONSTANT, int $GRAVITY_CONSTANT): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$imagick` | **\Imagick** |  |
| `$COMPOSITE_CONSTANT` | **int** |  |
| `$GRAVITY_CONSTANT` | **int** |  |





***

### localContrastImage

Attempts to increase the appearance of large-scale light-dark transitions.

```php
public localContrastImage(float $radius, float $strength): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$radius` | **float** |  |
| `$strength` | **float** |  |





***

### identifyImageType

Identifies the potential image type, returns one of the Imagick::IMGTYPE_* constants

```php
public identifyImageType(): int
```












***

### setImageAlpha

Sets the image to the specified alpha level. Will replace ImagickDraw::setOpacity()

```php
public setImageAlpha(float $alpha): bool
```








**Parameters:**

| Parameter | Type | Description |
|-----------|------|-------------|
| `$alpha` | **float** |  |





***


***
> Automatically generated on 2025-03-18
