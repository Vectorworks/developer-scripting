# AddSymToWallEdge

## Description
Procedure AddSymToWallEdge inserts a symbol in the referenced wall using the specified parameters to define placement. 

| Alignment                   | Constant |
|-----------------------------|----------|
| Centerline                  | 0        |
| Left Edge                   | 1        |
| Right Edge                  | 2        |
| Core Component Center       | 3        |
| Core Component Left Edge    | 4        |
| Core Component Right Edge   | 5        |

```pascal
PROCEDURE AddSymToWallEdge(
				h              : HANDLE;
				alongDistance  : REAL;
				heightDistance : REAL;
				flip           : BOOLEAN;
				right          : BOOLEAN;
				symbolName     : STRING;
				insertMode     : INTEGER);
```

```python
def vs.AddSymToWallEdge(h, alongDistance, heightDistance, flip, right, symbolName, insertMode):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to wall.|
|alongDistance|REAL|Offset distance from wall start of insertion point.|
|heightDistance|REAL|Elevation of symbol.|
|flip|BOOLEAN|Flip orientation of symbol.|
|right|BOOLEAN|Left-right orientation of symbol.|
|symbolName|STRING|Name of symbol to be inserted.|
|insertMode|INTEGER|Edge insertion mode.|

## Examples
[CreateWallObject](examples/CreateWallObject.md)

```pascal
BEGIN
WallHand := PickObject(x3,y3);
IF GetObject(kNNAIDSymbol) = NIL THEN
	ImportedNNASymbol := ImportTempSymbol;
AddSymToWallEdge(WallHand, 1', 0, FALSE, FALSE,kNNAIDSymbol,0);
SetRField(gIDHand, PIOName, '__WallUID', 'NEW');
propertyValue := '';

IF IsLineBasedWall(parentH) THEN BEGIN
	offsetDist := Distance(wallX, wallY, x, y);
	AddSymToWallEdge(parentH, offsetDist, theHeight, isFlipped, isRight, gParmN, 0);
END
```
```python
import vs

# Procedure AddSymToWallEdge inserts a symbol in the referenced wall using
# the specified parameters to define placement.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
alongDistance = 1.0
heightDistance = 2.0
flip = True
right = True
symbolName = 'MySymbol'
insertMode = 0

vs.AddSymToWallEdge(h, alongDistance, heightDistance, flip, right, symbolName, insertMode)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
