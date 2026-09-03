# FindObjAtPt_GetObj

## Description
Get an object from the find iterator

```pascal
FUNCTION FindObjAtPt_GetObj(
				finderID : LONGINT;
				objIndex : INTEGER): HANDLE;
```

```python
def vs.FindObjAtPt_GetObj(finderID, objIndex):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|finderID|LONGINT|   |
|objIndex|INTEGER|   |

## Remarks
List is 0-indexed.

## Examples
```pascal
  	BEGIN
  	TempObjHand := FindObjAtPt_GetObj(FinderID,I);
  	{AlrtDialog(Concat(GetType(TempObjHand)));}
IF GetType(TempObjHand) = 71 THEN
	BEGIN
	FloorThick := GetObjectVariableReal(h,173);
```
```python
import vs

# Get an object from the find iterator.
finderID = 1
objIndex = 1

objHandle = vs.FindObjAtPt_GetObj(finderID, objIndex)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
