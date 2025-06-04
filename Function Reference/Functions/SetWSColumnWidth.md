# SetWSColumnWidth

## Description
Sets the width of a column in the referenced worksheet.

SetWSColumnWidth allows width to be set for a range of columns. To set the width of a single worksheet column, specify identical values for the left/right column range boundaries.

```pascal
PROCEDURE SetWSColumnWidth(
				worksheet  : HANDLE;
				fromColumn : INTEGER;
				toColumn   : INTEGER;
				width      : INTEGER);
```

```python
def vs.SetWSColumnWidth(worksheet, fromColumn, toColumn, width):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|fromColumn|INTEGER|Leftmost column of column range.|
|toColumn|INTEGER|Rightmost column of column range.|
|width|INTEGER|New width of columns (in pixels).|

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
