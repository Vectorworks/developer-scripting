# AddSymToWall

## Description
Procedure AddSymToWall inserts a specified symbol into the referenced wall.

```pascal
PROCEDURE AddSymToWall(
				wallHd         : HANDLE;
				offDistance    : REAL;
				heightDistance : REAL;
				flip           : BOOLEAN;
				right          : BOOLEAN;
				symbolName     : STRING);
```

```python
def vs.AddSymToWall(wallHd, offDistance, heightDistance, flip, right, symbolName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wallHd|HANDLE|Handle to wall.|
|offDistance|REAL|Offset distance from wall start.|
|heightDistance|REAL|Elevation of symbol.|
|flip|BOOLEAN|Flipped status of symbol.|
|right|BOOLEAN|Left-right orientation of symbol.|
|symbolName|STRING|Name of symbol to insert in wall.|

## Remarks
See AddSymToWallEdge
[sd 8/13/98]

## Examples
eateWallObject}}

## See Also
VS Functions:
[AddSymToWallEdge](AddSymToWallEdge.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
