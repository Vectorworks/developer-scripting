# SetOrigin

## Description
Shifts the position of the document origin. The function does not modify the relative 
positions of objects in the document; the coordinate locations of objects, however, 
will change when the origin location is modified.

```pascal
PROCEDURE SetOrigin(
				x : REAL;
				y : REAL);
```

```python
def vs.SetOrigin(x, y):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|x|REAL|X-offset from current origin.|
|y|REAL|Y-offset from current origin.|

## Remarks
The difference between this and [[VS:SetOriginAbsolute]] is that this call <i>shifts</i> the origin the specified amount, where [{VS:SetOriginAbsolute]] sets the origin to the specified values.

See the &lt;a href=http://www.vectorlab.info/index.php?title=Absolute_Origin&gt;VectorLab article&lt;/a&gt; on origins by Gerard Jonker.

## Examples
#### VectorScript ####
```pascal
Rect(0,0,1,1);
SetOrigin(1,1);

{ Creates a rectangle with the bottom left point at coordinates (0,0), then moves the origin so that the top right point of the rectangle has coordinates (0,0). }
```
#### Python ####
```python

```

## See Also
VS Functions:
[SetOriginAbsolute](SetOriginAbsolute.md)

## Version
Availability: from All Versions

## Category
* [Document Settings](../Categories/Document%20Settings.md)
