# GetWSSubrowHeight

## Description
Return the height of a database subrow in the referenced worksheet.

```pascal
PROCEDURE GetWSSubrowHeight(
				worksheet   : HANDLE;
				databaserow : INTEGER;
				subrow      : INTEGER;
				VAR height  : INTEGER);
```

```python
def vs.GetWSSubrowHeight(worksheet, databaserow, subrow):
    return height
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|databaserow|INTEGER|The database row|
|subrow|INTEGER|The database subrow to be queried|
|height|INTEGER|Output parameter. Return the height (in pixels)|

## Examples
```pascal
GetWSSubrowHeight(worksheet, 1, 2, 3);
```
```python
import vs

# Return the height of a database subrow in the referenced worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
databaserow = 10
subrow = 10

result = vs.GetWSSubrowHeight(worksheet, databaserow, subrow)
```

## Version
Availability: from Vectorworks14.0

## Category
* [Worksheets](../Categories/Worksheets.md)
