# vstGetCurrPt2D

## Description
Returns the current location of the mouse.

```pascal
PROCEDURE vstGetCurrPt2D(
				VAR outX : REAL;
				VAR outY : REAL);
```

```python
def vs.vstGetCurrPt2D():
    return (outX, outY)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outX|REAL|Output parameter.|
|outY|REAL|Output parameter.|

## Examples
```pascal
begin
vstGetCurrpt2D(tempX, tempY);
For TmpIndex := 1 to gNumObjs DO
	BEGIN
	vstDrawCoordLine(ObjLoc[TmpIndex].X+OriginX, ObjLoc[TmpIndex].Y+OriginY,tempX+OriginX, tempY+OriginY);
	END;

begin
	If Is3dView then
		vstGetCurrpt3D(x2, y2, z2,result)
	else
		vstGetCurrpt2D(x2, y2);
	vstNumPts(numPts);
	if (numPts <> 0 ) then
	begin
		If Is3dView then
```
```python
import vs

# Returns the current location of the mouse.
outX, outY = vs.vstGetCurrPt2D()
vs.Message('vstGetCurrPt2D returned: ' + str((outX, outY)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
