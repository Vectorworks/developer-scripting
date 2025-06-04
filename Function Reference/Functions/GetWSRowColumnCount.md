# GetWSRowColumnCount

## Description
Returns the number of rows and columns in the referenced worksheet.

```pascal
PROCEDURE GetWSRowColumnCount(
				worksheet      : HANDLE;
				VAR numRows    : INTEGER;
				VAR numColumns : INTEGER);
```

```python
def vs.GetWSRowColumnCount(worksheet):
    return (numRows, numColumns)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|numRows|INTEGER|Number of rows in worksheet.|
|numColumns|INTEGER|Number of columns in worksheet.|

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
