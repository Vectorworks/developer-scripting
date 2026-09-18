# FindObjAtPt_Delete

## Description
Deletes the find object iterator

```pascal
PROCEDURE FindObjAtPt_Delete(finderID : LONGINT);
```

```python
def vs.FindObjAtPt_Delete(finderID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|finderID|LONGINT|   |

## Examples
```pascal
		IF  FloorHeight+FloorThick > TotalHeight THEN
			TotalHeight := FloorHeight+FloorThick;
		END;
   	END;
   FindObjAtPt_Delete(FinderID);
END;
```
```python
import vs

# Deletes the find object iterator.
finderID = 1

vs.FindObjAtPt_Delete(finderID)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
