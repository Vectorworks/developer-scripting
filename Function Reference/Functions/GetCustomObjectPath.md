# GetCustomObjectPath

## Description
Returns a handle to the path polygon of a path custom object.

```pascal
FUNCTION GetCustomObjectPath(objectHand : HANDLE): HANDLE;
```

```python
def vs.GetCustomObjectPath(objectHand):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHand|HANDLE|Handle to object.|

## Examples
```pascal
BEGIN
hPathObj := GetCustomObjectPath (ParentObj);
ALLOCATE pt [1..numVerts];
For I := 1 to numVerts DO
	GetPolyPt (hPathObj, I, pt [I].x, pt [I].y);
END;

BSB := SetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,FALSE);
BSB := SetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,FALSE);
GetVersion(version,vdummy,vdummy,vdummy);
IF (version > 9) THEN SetObjectVariableBoolean(parmHand, kFontPropertySelector, TRUE);
pathHand := GetCustomObjectPath(parmHand);
Path_Area_Handler(parmHand, pathHand, FALSE, TRUE, TRUE, FALSE);
gEdges := getvertnum(pathHand) - 1;
StraightenPoly(pathHand);
GetCurrUnits;

IF IsPolyClosed(GetCustomObjectPath(pluginH)) THEN
	gClosure := 1; {Set closure to None internally, but don't change the actual parameter}
```
```python
import vs

# Returns a handle to the path polygon of a path custom object.
objectHand = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetCustomObjectPath(objectHand)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
VS Functions:
[SetCustomObjectPath](SetCustomObjectPath.md)

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
