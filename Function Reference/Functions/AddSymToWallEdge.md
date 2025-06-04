# AddSymToWallEdge

## Description
Procedure AddSymToWallEdge inserts a symbol in the referenced wall using the specified parameters to define placement. 

{| class="wikitable_c"
|+ Table - Symbol Insertion Alignment
! Alignment !! Constant
|-
| Centerline
| style="text-align:center"| 0
|-
| Left Edge
| style="text-align:center"| 1
|-
| Right Edge
| style="text-align:center"| 2
|-
| Core Component Center
| style="text-align:center"| 3
|-
| Core Component Left Edge
| style="text-align:center"| 4
|-
| Core Component Right Edge
| style="text-align:center"| 5
|}

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
eateWallObject}}

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
