# SetLScale

## Description
Procedure SetLScale sets the scale of the referenced layer. 

Calculating the Scale:

To calculate the scale parameter from an architecural scale, the following formula may be used:
:denominator/numerator * true size(in inches) = ActualSize

For example, to calculate a scale of 3/8"=1'-0", the scale parameter would be 8/3 *12 = 32.

```pascal
PROCEDURE SetLScale(
				h     : HANDLE;
				scale : REAL);
```

```python
def vs.SetLScale(h, scale):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to layer.|
|scale|REAL|Scale value for layer.|

## Examples
==== VectorScript ====
```pascal
SetLScale(HandleToLayer,96);
{sets the referenced layer to a scale of 1/8&quot; = 1'}
```
==== Python ====
```python

```

## Version
Availability: from MiniCAD6.0

## Category
* [Layers](../Categories/Layers.md)
