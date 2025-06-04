# GetWSColumnWidth

## Description
Returns the width of a column in the referenced worksheet.

```pascal
PROCEDURE GetWSColumnWidth(
				worksheet : HANDLE;
				column    : INTEGER;
				VAR width : INTEGER);
```

```python
def vs.GetWSColumnWidth(worksheet, column):
    return width
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|column|INTEGER|Column to be queried.|
|width|INTEGER|Width of column (in pixels).|

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
