# GetWallBelCutPlClass

## Description
Gets the below cut plane class of the wall.

```pascal
FUNCTION GetWallBelCutPlClass(wall : HANDLE): LONGINT;
```

```python
def vs.GetWallBelCutPlClass(wall):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wall|HANDLE|The wall.|

## Examples
```pascal
resultN := GetWallBelCutPlClass(wall);
```
```python
import vs

# Gets the below cut plane class of the wall.
wall = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetWallBelCutPlClass(wall)
vs.Message('GetWallBelCutPlClass returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetWallBelCutPlClass](SetWallBelCutPlClass.md)

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
