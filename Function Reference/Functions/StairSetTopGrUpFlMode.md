# StairSetTopGrUpFlMode

## Description
Sets top graphic on other floor mode of stair - not recommended for use. See also StairGetTopGrUpFlMode.

```pascal
FUNCTION StairSetTopGrUpFlMode(
				stair                      : HANDLE;
				TopGraphicOnOtherFloorMode : INTEGER): BOOLEAN;
```

```python
def vs.StairSetTopGrUpFlMode(stair, TopGraphicOnOtherFloorMode):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stair|HANDLE|   |
|TopGraphicOnOtherFloorMode|INTEGER|   |

## Examples
```pascal
resultOK := StairSetTopGrUpFlMode(stair, 1);
```
```python
import vs

# Sets top graphic on other floor mode of stair - not recommended for use.
stair = vs.FSActLayer()  # handle to the first selected object on the active layer
TopGraphicOnOtherFloorMode = 0

ok = vs.StairSetTopGrUpFlMode(stair, TopGraphicOnOtherFloorMode)
if ok:
    vs.Message('StairSetTopGrUpFlMode succeeded')
else:
    vs.Message('StairSetTopGrUpFlMode failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Stairs](../Categories/Objects%20-%20Stairs.md)
