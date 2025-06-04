# GetCWidth

## Description
Function GetCWidth returns the column width of a cell in the referenced worksheet.

```pascal
FUNCTION GetCWidth(
				h   : HANDLE;
				row : INTEGER;
				col : INTEGER): INTEGER;
```

```python
def vs.GetCWidth(h, row, col):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to worksheet.|
|row|INTEGER|Worksheet row index.|
|col|INTEGER|Worksheet column index.|

## See Also
[GetWSColumnWidth | GetWSColumnWidth](GetWSColumnWidth%20| GetWSColumnWidth.md)

## Version
GetCWidth is obsolete as of VectorWorks 9.0, see [[VS:GetWSColumnWidth | GetWSColumnWidth]]

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
