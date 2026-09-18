# GetCurtainWallCutPl

## Description
Gets the curtain wall cut plane of the wall.

```pascal
FUNCTION GetCurtainWallCutPl(wall : HANDLE): REAL;
```

```python
def vs.GetCurtainWallCutPl(wall):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wall|HANDLE|The wall.|

## Examples
```pascal
resultVal := GetCurtainWallCutPl(wall);
```
```python
import vs

# Gets the curtain wall cut plane of the wall.
wall = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.GetCurtainWallCutPl(wall)
vs.Message('GetCurtainWallCutPl returned: ' + str(value))
```

## See Also
VS Functions:
[SetCurtainWallCutPl](SetCurtainWallCutPl.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
