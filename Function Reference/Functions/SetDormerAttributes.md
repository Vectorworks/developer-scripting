# SetDormerAttributes

## Description
Procedure SetDormerAttributes sets the attributes of a roof element in the referenced roof.

```pascal
PROCEDURE SetDormerAttributes(
				roofObject                 : HANDLE;
				dormerID                   : INTEGER;
				edgeIndex                  : INTEGER;
				cornerOffsetDistance       : REAL;
				isPerpOffset               : BOOLEAN;
				perpOrHeightOffsetDistance : REAL;
				symName                    : LONGINT;
				centerSymbol               : BOOLEAN;
				symOffsetDistance          : REAL);
```

```python
def vs.SetDormerAttributes(roofObject, dormerID, edgeIndex, cornerOffsetDistance, isPerpOffset, perpOrHeightOffsetDistance, symName, centerSymbol, symOffsetDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|
|dormerID|INTEGER|Index of dormer element.|
|edgeIndex|INTEGER|Index of roof edge.|
|cornerOffsetDistance|REAL|Corner offset distance.|
|isPerpOffset|BOOLEAN|Specifies perpendicular or height offset.|
|perpOrHeightOffsetDistance|REAL|Perpendicular or height offset distance.|
|symName|LONGINT|Index of dormer symbol.|
|centerSymbol|BOOLEAN|Specifies if symbol is centered.|
|symOffsetDistance|REAL|Symbol offset distance.|

## Remarks
This will fail if the dormerID identifies a skylight, or dormerID is not valid.

dormerID: Identifies the dormer for which to set the information.
edgeIndex: Index to which roof face this dormer is placed.  Value is one based.

cornerOffset: Distance from the vertex to the center of the dormer.
isPerpOffset: Determines the meaning of the next parameter.  Set to true for the value to be the plan distance from the outline to the front of the dormer.  Set to false for offsetValue to set the distance from the top of the dormer to the bearing height.
perpOrHeightOffset: Either the distance from the outline to the front of the dormer, or from the dormer roof to the floor.

symName: Symbol to place in the dormer, this is the window.
centerSymbol: Set to true to vertically center the symbol in the dormer.  Doing so causes the next parameter to be ignored.
Set to false to offset the symbol from the top of the dormer using the next parameter.
symOffset: Distance from top of the dormer to symbol insertion point.

## Examples
eateRoofOb}}

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
