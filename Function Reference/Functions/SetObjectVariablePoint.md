# SetObjectVariablePoint

## Description
Sets the value of a Vectorworks object property. Used with properties requiring a 2D or 3D point value.<BR>
<BR>
For specific object selector index values, see the Appendix.

```pascal
FUNCTION SetObjectVariablePoint(
				h     : HANDLE;
				index : INTEGER;
				p     : REAL): BOOLEAN;
```

```python
def vs.SetObjectVariablePoint(h, index, p):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|
|p|REAL|The object variable data point.|

## Examples
```pascal
		HCenter( GetVPCropObject( pioParentVPHand ), VPCropCenterPt.x, VPCropCenterPt.y );
	END;
END;
{ shifts the render background to the pioCMObjSavedLocPt (also the camera taget point) }
boo := SetObjectVariablePoint( pioParentVPHand, 1300, pioCMObjSavedLocPt.x, pioCMObjSavedLocPt.y, 0 );
```
```python
import vs

# Sets the value of a Vectorworks object property.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1
p = 1.0

ok = vs.SetObjectVariablePoint(h, index, p)
if ok:
    vs.Message('SetObjectVariablePoint succeeded')
else:
    vs.Message('SetObjectVariablePoint failed')
```

## See Also
VS Functions:
[GetObjectVariablePoint](GetObjectVariablePoint.md) 
| [GetObjectVariableBoolean](GetObjectVariableBoolean.md) 
| [SetObjectVariableBoolean](SetObjectVariableBoolean.md) 
| [GetObjectVariableHandle](GetObjectVariableHandle.md) 
| [SetObjectVariableHandle](SetObjectVariableHandle.md) 
| [GetObjectVariableInt](GetObjectVariableInt.md) 
| [SetObjectVariableInt](SetObjectVariableInt.md) 
| [GetObjectVariableLongInt](GetObjectVariableLongInt.md) 
| [SetObjectVariableLongInt](SetObjectVariableLongInt.md) 
| [GetObjectVariableReal](GetObjectVariableReal.md) 
| [SetObjectVariableReal](SetObjectVariableReal.md) 
| [GetObjectVariableString](GetObjectVariableString.md) 
| [SetObjectVariableString](SetObjectVariableString.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Object Info](../Categories/Object%20Info.md)
