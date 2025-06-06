# GetCellStr

## Description
Function GetCellStr returns the string value of a cell in the referenced worksheet.

```pascal
FUNCTION GetCellStr(
				h   : HANDLE;
				row : INTEGER;
				col : INTEGER): STRING;
```

```python
def vs.GetCellStr(h, row, col):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to worksheet.|
|row|INTEGER|Worksheet row index.|
|col|INTEGER|Worksheet column index.|

## See Also
Functions:
* [GetWSCellString](GetWSCellString.md)
* [GetWSSubrowCellString](GetWSSubrowCellString.md)
* [GetWSCellStringN](GetWSCellStringN.md) 
* [GetWSSubrowCellStrN](GetWSSubrowCellStrN.md)

## Version
GetCellStr is obsolete as of VectorWorks 9.0, see new [ GetWSCellString](GetWSCellString.md) and [ GetWSSubrowCellString](GetWSSubrowCellString.md), [ GetWSCellStringN](GetWSCellStringN.md) and [ GetWSSubrowCellStrN](GetWSSubrowCellStrN.md)

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
