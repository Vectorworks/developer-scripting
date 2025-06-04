# InsertSymbol

## Description
Procedure InsertSymbol places a specified symbol into a wall.

```pascal
PROCEDURE InsertSymbol(
				offsetDistance : REAL;
				heightDistance : REAL;
				flipped        : BOOLEAN;
				right          : BOOLEAN;
				capped         : BOOLEAN;
				symbolName     : STRING);
```

```python
def vs.InsertSymbol(offsetDistance, heightDistance, flipped, right, capped, symbolName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|offsetDistance|REAL|Offset distance from wall start.|
|heightDistance|REAL|Elevation of symbol.|
|flipped|BOOLEAN|Flip orientation of symbol.|
|right|BOOLEAN|Left-right orientation of symbol.|
|capped|BOOLEAN|Cap wall breaks.|
|symbolName|STRING|Name of symbol to be inserted in wall.|

## Examples
==== VectorScript ====
```pascal
MoveTo(3,1);
WallTo(5',5');
InsertSymbol(1',False,False,True,'Door');
{inserts the symbol 'Door' at 1' from the start point of the last wall segment}
```
==== Python ====
```python

```

## See Also
VS Functions:
[AddSymToWall](AddSymToWall.md) 
| [AddSymToWallEdge](AddSymToWallEdge.md)

## Version
Availability: from MiniCAD4.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
