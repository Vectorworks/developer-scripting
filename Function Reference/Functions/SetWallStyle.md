# SetWallStyle

## Description
Applies the given Wall Style to the given wall, aligning to the given offsets.

```pascal
FUNCTION SetWallStyle(
				theWall              : HANDLE;
				wallStyle            : STRING;
				selectedOffDistance  : REAL;
				replacingOffDistance : REAL): BOOLEAN;
```

```python
def vs.SetWallStyle(theWall, wallStyle, selectedOffDistance, replacingOffDistance):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theWall|HANDLE|The wall.|
|wallStyle|STRING|The Wall Style to apply.|
|selectedOffDistance|REAL|The offset of the wall to align to.|
|replacingOffDistance|REAL|The offset of the Wall Style to align to.|

## Examples
Example
```pascal
PROCEDURE Example;
VAR
theWall :HANDLE;
wallStyle :STRING;
selectedOffDistance :REAL;
replacingOffDistance :REAL;
BEGIN
theWall := FSActLayer;
wallStyle := 'Ext-2x4-Brick veneer';
selectedOffDistance := 0;
replacingOffDistance := 0;
Message(SetWallStyle(theWall, wallStyle, selectedOffDistance, replacingOffDistance));
END;
RUN(Example);
```
==== Python ====
```python

```

## See Also
VS Functions:
[GetWallStyle](GetWallStyle.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
