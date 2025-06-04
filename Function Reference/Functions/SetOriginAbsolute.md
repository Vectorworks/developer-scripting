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
The difference between [[VS:SetOrigin]] and [[VS:SetOriginAbsolute]] is that SetOrigin <i>shifts</i> the origin the specified amount, where [[VS:SetOriginAbsolute]] <i>sets</i> the origin to the specified values.

See the &lt;a href=http://www.vectorlab.info/index.php?title=Absolute_Origin&gt;VectorLab article&lt;/a&gt; on origins by Gerard Jonker.

## See Also
VS Functions:
[SetOrigin](SetOrigin.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
