# GetCAlign

## Description
Function GetCAlign returns the alignment value of a cell in the referenced worksheet. 


**Table - Worksheet Cell Alignment**

| Alignment | Constant |
|-----------|----------|
| General   | 1        |
| Left      | 2        |
| Right     | 3        |
| Center    | 4        |

```pascal
FUNCTION GetCAlign(
				h   : HANDLE;
				row : INTEGER;
				col : INTEGER): INTEGER;
```

```python
def vs.GetCAlign(h, row, col):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to worksheet.|
|row|INTEGER|Worksheet row index.|
|col|INTEGER|Worksheet column index.|

## Examples
#### VectorScript ####
```pascal
AlignmentMode := GetCAlign(WSheetHd, 4, 5);
```
#### Python ####
```python
AlignmentMode = vs.GetCAlign(WSheetHd, 4, 5)
```

## See Also
[GetWSCellAlignment | GetWSCellAlignment](GetWSCellAlignment%20| GetWSCellAlignment.md)

## Version
GetCAlign is obsolete as of VectorWorks 9.0, see new [[VS:GetWSCellAlignment| GetWSCellAlignment]]

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
