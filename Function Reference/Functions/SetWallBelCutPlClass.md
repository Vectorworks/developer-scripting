# SetWallBelCutPlClass

## Description
Sets the below cut plane class of the wall.

```pascal
PROCEDURE SetWallBelCutPlClass(
				wall               : HANDLE;
				belowCutPlaneClass : LONGINT);
```

```python
def vs.SetWallBelCutPlClass(wall, belowCutPlaneClass):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wall|HANDLE|The wall.|
|belowCutPlaneClass|LONGINT|The below cut plane class.|

## Examples
```pascal
SetWallBelCutPlClass(wall, 1);
```
```python
import vs

# Sets the below cut plane class of the wall.
wall = vs.FSActLayer()  # handle to the first selected object on the active layer
belowCutPlaneClass = 1

vs.SetWallBelCutPlClass(wall, belowCutPlaneClass)
```

## See Also
VS Functions:
[GetWallBelCutPlClass](GetWallBelCutPlClass.md)

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
