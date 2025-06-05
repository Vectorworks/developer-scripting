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
[IsWSCellNumber](IsWSCellNumber.md), [IsWSSubrowCellNumber](IsWSSubrowCellNumber.md)

## Version
CellHasNum is obsolete as of VectorWorks 9.0, see [IsWSCellNumber](IsWSCellNumber.md), [IsWSSubrowCellNumber](IsWSSubrowCellNumber.md)

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
