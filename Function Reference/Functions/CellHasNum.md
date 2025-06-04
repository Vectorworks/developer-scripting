# CellHasNum

## Description
Function CellHasNum returns TRUE if the specified cell of a referenced worksheet contains a value or an equation which returns a numeric value.

```pascal
FUNCTION CellHasNum(
				h   : HANDLE;
				row : INTEGER;
				col : INTEGER): BOOLEAN;
```

```python
def vs.CellHasNum(h, row, col):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to worksheet.|
|row|INTEGER|Worksheet row index.|
|col|INTEGER|Worksheet column index.|

## See Also
[IsWSCellNumber | IsWSCellNumber](IsWSCellNumber%20| IsWSCellNumber.md), [IsWSSubrowCellNumber | IsWSSubrowCellNumber](IsWSSubrowCellNumber%20| IsWSSubrowCellNumber.md)

## Version
CellHasNum is obsolete as of VectorWorks 9.0, see [[VS:IsWSCellNumber | IsWSCellNumber]], [[VS:IsWSSubrowCellNumber | IsWSSubrowCellNumber]]

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
