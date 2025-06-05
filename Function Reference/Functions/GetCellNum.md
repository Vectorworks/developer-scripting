# GetCellNum

## Description
Function GetCellNum returns the numeric value of a cell in the referenced worksheet.

```pascal
FUNCTION GetCellNum(
				h   : HANDLE;
				row : INTEGER;
				col : INTEGER): REAL;
```

```python
def vs.GetCellNum(h, row, col):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to worksheet.|
|row|INTEGER|Worksheet row index.|
|col|INTEGER|Worksheet column index.|

## See Also
[GetWSCellValue](GetWSCellValue.md), [GetWSSubrowCellValue](GetWSSubrowCellValue.md)

## Version
GetCellNum is obsolete as of VectorWorks 9.0, see new [ GetWSCellValue](GetWSCellValue.md) and [ GetWSSubrowCellValue](GetWSSubrowCellValue.md)

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
