# CellHasStr

## Description
Function CellHasStr returns TRUE if the specified cell of a referenced worksheet contains a value or an equation which returns a string value.

```pascal
FUNCTION CellHasStr(
				h   : HANDLE;
				row : INTEGER;
				col : INTEGER): BOOLEAN;
```

```python
def vs.CellHasStr(h, row, col):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to worksheet.|
|row|INTEGER|Worksheet row index.|
|col|INTEGER|Worksheet column index.|

## See Also
[IsWSCellString | IsWSCellString](IsWSCellString%20| IsWSCellString.md), [IsWSSubrowCellString | IsWSSubrowCellString](IsWSSubrowCellString%20| IsWSSubrowCellString.md)

## Version
CellHasStr is obsolete as of VectorWorks 9.0, see [IsWSCellString](IsWSCellString.md), [IsWSSubrowCellString](IsWSSubrowCellString.md)

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
