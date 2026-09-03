# FindObjAtPt_GetCount

## Description
Gets the number of objects in the find iterator

```pascal
FUNCTION FindObjAtPt_GetCount(finderID : LONGINT): INTEGER;
```

```python
def vs.FindObjAtPt_GetCount(finderID):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|finderID|LONGINT|   |

## Examples
```pascal
GetSymLoc(h,x,y);
   FinderID := FindObjAtPt_Create(ActLayer,1,1,x,y,1");
   NumObjsFound := FindObjAtPt_GetCount(FinderID);
   {AlrtDialog(Concat(NumObjsFound));}
   For I := 0 to NumObjsFound-1 DO
   	BEGIN
   	TempObjHand := FindObjAtPt_GetObj(FinderID,I);
```
```python
import vs

# Gets the number of objects in the find iterator.
finderID = 1

count = vs.FindObjAtPt_GetCount(finderID)
vs.Message('FindObjAtPt_GetCount returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
