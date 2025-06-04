# GetDormerAttributes

## Description
Procedure GetDormerAttributes returns the attributes of a roof element in the referenced roof.

```pascal
PROCEDURE GetDormerAttributes(
				roofObject             : HANDLE;
				dormerID               : INTEGER;
				VAR edgeIndex          : INTEGER;
				VAR cornerOffset       : REAL;
				VAR isPerpOffset       : BOOLEAN;
				VAR perpOrHeightOffset : REAL;
				VAR symName            : LONGINT;
				VAR centerSymbol       : BOOLEAN;
				VAR symOffset          : REAL);
```

```python
def vs.GetDormerAttributes(roofObject, dormerID):
    return (edgeIndex, cornerOffset, isPerpOffset, perpOrHeightOffset, symName, centerSymbol, symOffset)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|
|dormerID|INTEGER|Index of dormer element.|
|edgeIndex|INTEGER|Index of roof edge.|
|cornerOffset|REAL|Returns offset from roof edge corner.|
|isPerpOffset|BOOLEAN|Returns whether perpendicular offset was used.|
|perpOrHeightOffset|REAL|Returns perpendicualr or height offset.|
|symName|LONGINT|Returns index of dormer symbol.|
|centerSymbol|BOOLEAN|Returns whether symbol was centered.|
|symOffset|REAL|Returns symbol offset distance.|

## Remarks
This will fail if the dormerID identifies a skylight, or dormerID is not valid.

dormerID: Identifies the dormer for which to retrieve the information.
edgeIndex: Index to which roof face this skylight is placed.  Value is one based.

cornerOffset: Distance from the vertex to the center of the dormer.
isPerpOffset: Determines the meaning of the next parameter.  Set to true for the value to be the plan distance from the outline to the front of the dormer.  Set to false for offsetValue to set the distance from the top of the dormer to the bearing height.
perpOrHeightOffset: Either the distance from the outline to the front of the dormer, or from the dormer roof to the floor.

symName: Symbol to place in the dormer, this is the window.
centerSymbol: Set to true to vertically center the symbol in the dormer.  Doing so causes the next parameter to be ignored.
Set to false to offset the symbol from the top of the dormer using the next parameter.
symOffset: Distance from top of the dormer to symbol insertion point.

## See Also
VS Functions:
[Index2Name](Index2Name.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
