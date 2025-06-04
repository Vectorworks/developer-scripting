# GetWSRowHeight

## Description
Returns the height of a row in the referenced worksheet.

```pascal
PROCEDURE GetWSRowHeight(
				worksheet  : HANDLE;
				row        : INTEGER;
				VAR height : INTEGER);
```

```python
def vs.GetWSRowHeight(worksheet, row):
    return height
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row to be queried.|
|height|INTEGER|Height of row (in pixels).|

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
