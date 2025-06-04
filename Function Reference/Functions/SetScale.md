# SetScale

## Description
Procedure SetScale sets the drawing scale of the active layer of the document.

<I>Calculating the Scale</I><P>
To calculate the scale parameter from an architecural scale, the following formula may be used :<P>

<CENTER>denominator/numerator * true size(in inches) = ActualSize</CENTER><P>

For example, to calculate a scale of 3/8"=1'-0", the scale parameter would be 8/3 *12 = 32.

```pascal
PROCEDURE SetScale(actualSize : REAL);
```

```python
def vs.SetScale(actualSize):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|actualSize|REAL|Drawing scale factor.|

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
