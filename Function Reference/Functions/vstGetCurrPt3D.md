# vstGetCurrPt3D

## Description
Returns the current location of the mouse.

```pascal
PROCEDURE vstGetCurrPt3D(
				VAR outX : REAL;
				VAR outY : REAL;
				VAR outZ : REAL;
				result   : BOOLEAN);
```

```python
def vs.vstGetCurrPt3D(result):
    return (outX, outY, outZ)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outX|REAL|Output parameter.|
|outY|REAL|Output parameter.|
|outZ|REAL|Output parameter.|
|result|BOOLEAN|   |

## Remarks
In Python, the result boolean input variable doesn't seem to do anything.

## Examples
```pascal
Begin
vstGetCurrpt3D(tempX,tempY,tempZ,result);
For TmpIndex := 1 to gNumObjs DO
begin
	vstDrawCoordLine3D(ObjLoc[TmpIndex].X+OriginX, ObjLoc[TmpIndex].Y+OriginY,0,tempX+OriginX, tempY+OriginY,0);
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
result = True

outX, outY, outZ = vs.vstGetCurrPt3D(result)
vs.Message('vstGetCurrPt3D returned: ' + str((outX, outY, outZ)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
