# GetWSSubrowActualCellString

## Description
Returns the actual string in a database subrow cell.

```pascal
PROCEDURE GetWSSubrowActualCellString(
				worksheet      : HANDLE;
				row            : INTEGER;
				column         : INTEGER;
				subrow         : INTEGER;
				VAR cellString : STRING);
```

```python
def vs.GetWSSubrowActualCellString(worksheet, row, column, subrow):
    return cellString
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|   |
|row|INTEGER|   |
|column|INTEGER|   |
|subrow|INTEGER|   |
|cellString|STRING|   |

## Remarks
Gets the specified worksheet subrow cell's actual string.
WARNING: Because database subrow cells and their contents are dynamically created based on the current database of objects and the current critieria string any return values from this function are not guaranteed to be correct beyond this function call. Use this function carefully and at your own risk.

## Examples
```pascal
GetWSSubrowActualCellString(worksheet, 1, 2, 3, 'Example');
```
```python
import vs

# Returns the actual string in a database subrow cell.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
row = 10
column = 5
subrow = 10

text = vs.GetWSSubrowActualCellString(worksheet, row, column, subrow)
vs.Message('GetWSSubrowActualCellString returned: ' + str(text))
```

## Version
Availability: from VectorWorks13.0

## Category
* [Worksheets](../Categories/Worksheets.md)
