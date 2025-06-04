# HWallWidth

## Description
Procedure HWallWidth sets the wall width of the referenced wall object.

```pascal
PROCEDURE HWallWidth(
				wallHd        : HANDLE;
				widthDistance : REAL);
```

```python
def vs.HWallWidth(wallHd, widthDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wallHd|HANDLE|Handle to wall.|
|widthDistance|REAL|New wall width.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
targetWall, sourceWall :HANDLE;
cnt1, cnt2, cavs :INTEGER;
BEGIN
targetWall := FSActLayer;
MoveTo(0,0);
WallTo(1,0);
sourceWall := LNewObj;
cavs := GetObjectVariableInt(sourceWall, 199);
HWallWidth(targetWall, WallWidth(sourceWall));
SetObjectVariableInt(targetWall, 199, cavs);
FOR cnt2 := 0 TO cavs - 1 DO BEGIN
SetObjectVariableBoolean(targetWall, 240 + cnt2, GetObjectVariableBoolean(sourceWall, 240 + cnt2)); {cavity is pair}
SetObjectVariableReal   (targetWall, 200 + cnt2, GetObjectVariableReal   (sourceWall, 200 + cnt2)); {left offset}
SetObjectVariableReal   (targetWall, 220 + cnt2, GetObjectVariableReal   (sourceWall, 220 + cnt2)); {right offset}
SetObjectVariableLongInt(targetWall, 260 + cnt2, GetObjectVariableLongInt(sourceWall, 260 + cnt2)); {cavity fill}
SetObjectVariableInt    (targetWall, 280 + cnt2, GetObjectVariableInt    (sourceWall, 280 + cnt2)); {pen weight}
SetObjectVariableInt    (targetWall, 300 + cnt2, GetObjectVariableInt    (sourceWall, 300 + cnt2)); {pen style}
END;
ResetObject(targetWall);
DelObject(sourceWall);
END;
RUN(Example);
```
#### Python ####
```python

```

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
