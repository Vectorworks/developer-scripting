# OLDGetHangPointAt

## Description
Get hang point for given index of the specified load for the parametric object

```pascal
PROCEDURE OLDGetHangPointAt(
				handle      : HANDLE;
				loadIndex   : INTEGER;
				pointIndex  : LONGINT;
				VAR point   : VECTOR;
				VAR hasLoad : BOOLEAN);
```

```python
def vs.OLDGetHangPointAt(handle, loadIndex, pointIndex):
    return (point, hasLoad)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|loadIndex|INTEGER|   |
|pointIndex|LONGINT|   |
|point|VECTOR|   |
|hasLoad|BOOLEAN|   |

## Examples
```pascal
BEGIN
	OLDGetHangPointAt( loadObj, loadIndex, 1, prevPt, prevHasLoad );
	FOR index := 2 TO versCount DO
	BEGIN
		OLDGetHangPointAt( loadObj, loadIndex, index, currPt, currHasLoad );
		IF prevHasLoad THEN

BEGIN
	OLDGetHangPointAt( tempHandle, 0, 1, resultPt, currHasLoad);

{Object To World}
OLDGetHangPointAt( ghParm, 0, 1, resultPt, currHasLoad);
GetSymLoc3D(ghParm, symLoc.x, symLoc.y, symLoc.z);
symLoc.z := symLoc.z + resultPt.z;
resultPt.z := 0;
symRot := GetSymRot(ghParm);
```
```python
import vs

# Get hang point for given index of the specified load for the parametric object.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
loadIndex = 1
pointIndex = 1

pt, hasLoad = vs.OLDGetHangPointAt(handle, loadIndex, pointIndex)
vs.Message('OLDGetHangPointAt returned: ' + str((pt, hasLoad)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
