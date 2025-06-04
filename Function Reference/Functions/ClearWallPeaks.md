# ClearWallPeaks

## Description
Removes all wall peaks from the referenced wall.

```pascal
PROCEDURE ClearWallPeaks(h : HANDLE);
```

```python
def vs.ClearWallPeaks(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to wall.|

## Remarks
remove all peaks in this wall

Julian says that this is broken for round walls, but I haven't verified it (nor checked the bug list).

It works as expected on VW 13.

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
