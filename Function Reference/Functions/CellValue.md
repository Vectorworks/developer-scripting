# CellValue

## Description
Function CellValue returns the numeric value of a specified cell in the active worksheet. If the specified cell is not a numeric type, then this function returns 0.

```pascal
FUNCTION CellValue(
				row    : INTEGER;
				column : INTEGER): REAL;
```

```python
def vs.CellValue(row, column):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|row|INTEGER|Worksheet row index.|
|column|INTEGER|Worksheet column index.|

## Remarks
Returns the floating point representation of the current worksheet's cell specified by &quot;row&quot; and &quot;column&quot; numbers.  If the specified cell is not a numeric type, then this function returns 0. [sd 8/13/98]

## See Also
[GetWSCellValue | GetWSCellValue](GetWSCellValue%20| GetWSCellValue.md), [GetWSSubrowCellValue | GetWSSubrowCellValue](GetWSSubrowCellValue%20| GetWSSubrowCellValue.md)

## Version
CellValue is obsolete as of VectorWorks 9.0, see [[VS:GetWSCellValue | GetWSCellValue]], [[VS:GetWSSubrowCellValue | GetWSSubrowCellValue]]

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
