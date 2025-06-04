# IsWSSubrowCellNumber

## Description
Returns whether a specified database subrow cell contains a numeric value.

```pascal
FUNCTION IsWSSubrowCellNumber(
				worksheet : HANDLE;
				row       : INTEGER;
				column    : INTEGER;
				subrow    : INTEGER): BOOLEAN;
```

```python
def vs.IsWSSubrowCellNumber(worksheet, row, column, subrow):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Database row to be queried.|
|column|INTEGER|Column to be queried.|
|subrow|INTEGER|Index of subrow to be queried.|

## Remarks
Determines if the specified worksheet subrow cell's contents is a numerical value.
WARNING: Because database subrow cells and their contents are dynamically created based on the current database of objects and the current critieria string any return values from this function are not guaranteed to be correct beyond this function call. Use this function carefully and at your own risk.

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
