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

## Examples
```pascal
BEGIN
	GetOrigin (x0, y0);
	SetOriginAbsolute (0, 0);

kToolCompleteEventID: BEGIN
	IF ResourceIsOK THEN
	ptMode := kPolyPointTool;
	GetOrigin(origin.x, origin.y);
	SetOriginAbsolute(0, 0);
	sheetLayerH := ActLayer;
	bSheetLayer := FALSE;
	IF (sheetLayerH <> nil) & (GetObjectVariableInt(sheetLayerH, 154) = 2) THEN BEGIN
		boo := GetSheetLayerUserOrigin(sheetLayerH, sheetOrigin.x, sheetOrigin.y);

			Layer(LayerChStr);
		MyLayerScale := GetLScale(ActLayer);
		END;
GetOrigin(Xo,Yo);
SetOriginAbsolute(0,0);
PlaceWorksheet;
SetOriginAbsolute(Xo,Yo);
IF MaxError THEN AlrtDialog(kStrMaxError);
IF DisplayErrorMessage THEN AlrtDialog(kStrOverlap);
```
```python
import vs

# Procedure SetOriginAbsolute sets the position of the origin relative to the
# center of the document drawing space.
xValue = 1.0
yValue = 2.0

vs.SetOriginAbsolute(xValue, yValue)
```

## See Also
VS Functions:
[SetOrigin](SetOrigin.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
