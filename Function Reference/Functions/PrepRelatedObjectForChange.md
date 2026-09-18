# PrepRelatedObjectForChange

## Description
Prepares some other related object for a change thats about to occur.

```pascal
PROCEDURE PrepRelatedObjectForChange(objectAboutToBeChange : HANDLE);
```

```python
def vs.PrepRelatedObjectForChange(objectAboutToBeChange):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectAboutToBeChange|HANDLE|The object to be prepared for a change|

## Remarks
This call adds an eBeforeModify primitive to the specified object provided that the undo system is currently building an undo event.  

Does this mean that the object is sent an event, and if so, what is the event code?

## Examples
```pascal
PrepRelatedObjectForChange(tempH1);
selHandles[TmpIndex] := ConvertToPolyline(selHandles[TmpIndex]);

	cen_pt.x := ObjLoc[TmpIndex].x+1";
	cen_pt.y := ObjLoc[TmpIndex].y+1";
	END;
tempH1 := selHandles[TmpIndex];
PrepRelatedObjectForChange(tempH1);
selHandles[TmpIndex] := ConvertToPolyline(selHandles[TmpIndex]);
tempH := CreateSeatLayoutObj(selHandles[TmpIndex], cen_pt, SelectedSymbolName, Auto);
END;
```
```python
import vs

# Prepares some other related object for a change thats about to occur.
objectAboutToBeChange = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.PrepRelatedObjectForChange(objectAboutToBeChange)
```

## Version
Availability: from VectorWorks12.5

## Category
* [Utility](../Categories/Utility.md)
