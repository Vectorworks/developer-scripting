# GetSkylight

## Description
Function GetSkylight returns the definition attributes of a specified skylight in the referenced roof object.

```pascal
PROCEDURE GetSkylight(
				roofObject       : HANDLE;
				skylightID       : INTEGER;
				VAR edgeIndex    : INTEGER;
				VAR cornerOffset : REAL;
				VAR perpOffset   : REAL;
				VAR symName      : LONGINT);
```

```python
def vs.GetSkylight(roofObject, skylightID):
    return (edgeIndex, cornerOffset, perpOffset, symName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|
|skylightID|INTEGER|Index of skylight element.|
|edgeIndex|INTEGER|Index of roof edge associated with skylight.|
|cornerOffset|REAL|Offset of skylight from corner.|
|perpOffset|REAL|Offset of skylight from roof edge.|
|symName|LONGINT|Name of skylight symbol.|

## Remarks
skylightID: Identifier for this skylight.  Value is returned by CreateSkylight().
edgeIndex: Index to which roof face this skylight is placed.  Value is one based.
cornerOffset: Top/Plan distance from vertex referenced by 'edgeIndex' to center of skylight.  This distance is parallel to the roof outline as defined by: vertex[edgeindex+1] - vertex[edgeIndex].
perpOffset: Top/Plan distance from roof outline to center of skylight.
symName: Skylight symbol to place in the roof.

## Examples
==== VectorScript ====
```pascal
GetSkylight(roofHandle,skylightID,edgeID,cOff,pOff,symID);
symbolName:=Index2Name(symID);
```
==== Python ====
```python
edgeID,cOff,pOff,symID = vs.GetSkylight(roofHandle,skylightID)
```

## See Also
VS Functions:
[Index2Name](Index2Name.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
