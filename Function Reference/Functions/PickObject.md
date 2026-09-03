# PickObject

## Description
Function PickObject returns a handle to an object in the document. The function receives a coordinate location, specified by parameter p, and checks this location for the presence of an object. If an object exists at the location, the function returns a handle to the object.

```pascal
FUNCTION PickObject(pX,pY : REAL): HANDLE;
```

```python
def vs.PickObject(p):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Coordinate location to test for object.|

## Remarks
Only picks objects on the active class &amp; layer, or on other classes/layers if the class/layer options are set to Show/Snap/Modify (respectively). Essentially, it will only pick an object that you could have picked manually with the Selection Tool. Same goes for the GetPickObjectInfo function.

PickObject & HCenter (when used together?) are less likely to produce incorrect results if you zoom in first.

## Examples
[IsolateLayer](examples/IsolateLayer.md)

```pascal
IF Ang2BearingStr(tmpAngle) <> GetText (PickObject (ptX + tmpVector[1] + labelVector[1], ptY + tmpVector[2] + labelVector[2])) THEN
	CreateText(Ang2BearingStr(tmpAngle));

		THEN temp_b := GetPickObjectInfo(pt1.x,pt1.y,gGroupH,gLine,temp_i)
		ELSE BEGIN
			zoomF := GetZoom;
			SetZoom (100000);
			gLine := PickObject(pt1.x,pt1.y);
			SetZoom (zoomF);
{
message (' *** pt1.x = ',pt1.x,'    pt1.y = ',pt1.y,'    gLine = ',gLine, '(',gettype(gLine),')', '    gParmH = ',gParmH, '(',gettype(gParmH),')');
}

BEGIN
	target := PickObject(pt.x, pt.y);
	WHILE (target = NIL) & (YNDialog(Concat(GetPlugInString(3000), msg, GetPlugInString(3003)))) DO BEGIN
		IF msg = GetPlugInString(3001)
			THEN GetPt(pt.x, pt.y)
			ELSE GetPtL(pt1.x, pt1.y, pt.x, pt.y);
```
```python
import vs

# Function PickObject returns a handle to an object in the document.
p = (0, 0)

objHandle = vs.PickObject(p)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
VS Functions:
[GetPickObjectInfo](GetPickObjectInfo.md) 
| [ForEachObjectAtPoint](ForEachObjectAtPoint.md)

## Version
Availability: from All Versions

## Category
* [Utility](../Categories/Utility.md)
