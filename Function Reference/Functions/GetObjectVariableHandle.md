# GetObjectVariableHandle

## Description
Returns the value of a VectorWorks object property.

```pascal
FUNCTION GetObjectVariableHandle(
				h     : HANDLE;
				index : INTEGER): HANDLE;
```

```python
def vs.GetObjectVariableHandle(h, index):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|index|INTEGER|   |

## Examples
```pascal
elevatorHandle := GetObjectVariableHandle( objectHandle, -111 );
IF elevatorHandle <> NIL THEN
BEGIN
	elevatorWall := GetParent( elevatorHandle );
	IF elevatorWall <> NIL THEN

BEGIN
	originalWall_h := wall_h;
	planViewWallOffset.x := 0;
	planViewWallOffset.y := 0;
	planViewWall_h := GetObjectVariableHandle(wall_h, 620);

BEGIN
IF NOT (GetPref(531) & (GetObjectVariableHandle(gParmH, 1646) = NIL)) THEN
	BEGIN
	FixtureLabel := GetPlugInString(3001);
	MoveTo(0,0);
	CreateText(FixtureLabel);
	SetFPat(LNewObj, 0);
	SetTextSize(LNewObj,0,1,10+p2D_Scale_Factor);
```
```python
import vs

# Returns the value of a VectorWorks object property.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1

objHandle = vs.GetObjectVariableHandle(h, index)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Object Info](../Categories/Object%20Info.md)
