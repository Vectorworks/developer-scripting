# SetOriginAbsolute

## Description
Procedure SetOriginAbsolute sets the position of the origin relative to the center of the document drawing space.

```pascal
PROCEDURE SetOriginAbsolute(
				xValue : REAL;
				yValue : REAL);
```

```python
def vs.SetOriginAbsolute(xValue, yValue):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|xValue|REAL|X coordinate of origin.|
|yValue|REAL|Y coordinate of origin.|

## Remarks
The difference between [SetOrigin](SetOrigin.md) and [SetOriginAbsolute](SetOriginAbsolute.md) is that SetOrigin *shifts* the origin the specified amount, where [SetOriginAbsolute](SetOriginAbsolute.md) *sets* the origin to the specified values.

See the [VectorLab article](http://www.vectorlab.info/index.php?title=Absolute_Origin) on origins by Gerard Jonker.

## See Also
VS Functions:
[SetOrigin](SetOrigin.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
