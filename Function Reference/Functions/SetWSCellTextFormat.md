# SetWSCellTextFormat

## Description
Sets text format settings for a cell in the referenced worksheet.

SetWSCellTextFormat allows text formatting to be set for a rectangular range of cells. To set the formatting of a single cell, specify identical values for the top/bottom and left/right range boundaries.

**Table - Text Style**

| Style     | Constant |
|-----------|----------|
| Plain     | 0        |
| Bold      | 1        |
| Italic    | 2        |
| Underline | 4        |
| Outline   | 8        |
| Shadowed  | 16       |

```pascal
PROCEDURE SetWSCellTextFormat(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				fontIndex   : INTEGER;
				size        : INTEGER;
				style       : INTEGER);
```

```python
def vs.SetWSCellTextFormat(worksheet, topRow, leftColumn, bottomRow, rightColumn, fontIndex, size, style):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|topRow|INTEGER|Top row of cell range.|
|leftColumn|INTEGER|Leftmost column of cell range.|
|bottomRow|INTEGER|Bottom row of cell range.|
|rightColumn|INTEGER|Rightmost column of cell range.|
|fontIndex|INTEGER|Font index for cell text.|
|size|INTEGER|Font size for cell text.|
|style|INTEGER|Font style for cell text.|

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
