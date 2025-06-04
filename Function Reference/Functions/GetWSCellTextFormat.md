# GetWSCellTextFormat

## Description
Returns text format settings for a cell in the referenced worksheet.

{| class="wikitable_c"
|+ Table - Text Style
! Style
! Constant
|-
| Plain
| style="text-align:center"| 0
|-
| Bold
| style="text-align:center"| 1
|-
| Italic
| style="text-align:center"| 2
|-
| Underline
| style="text-align:center"| 4
|-
| Outline
| style="text-align:center"| 8
|-
| Shadowed
| style="text-align:center"| 16
|}

```pascal
PROCEDURE GetWSCellTextFormat(
				worksheet     : HANDLE;
				row           : INTEGER;
				column        : INTEGER;
				VAR fontIndex : INTEGER;
				VAR size      : INTEGER;
				VAR style     : INTEGER);
```

```python
def vs.GetWSCellTextFormat(worksheet, row, column):
    return (fontIndex, size, style)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row of cell to be queried.|
|column|INTEGER|Column of cell to be queried.|
|fontIndex|INTEGER|Font index of cell text.|
|size|INTEGER|Font size of cell text.|
|style|INTEGER|Font style of cell text.|

## Remarks
Note: Outline and Shadow only display on the Mac

FontStyle integer is the sum of applicable attributes.

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
