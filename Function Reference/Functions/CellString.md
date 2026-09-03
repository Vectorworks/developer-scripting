# CellString

## Description
Function CellString returns the string of a specified cell in the active worksheet

```pascal
FUNCTION CellString(
				row    : INTEGER;
				column : INTEGER): STRING;
```

```python
def vs.CellString(row, column):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|row|INTEGER|Worksheet row index.|
|column|INTEGER|Worksheet column index.|

## Remarks
Returns the string representation of the current worksheet's cell specified by 'row' and 'column' numbers. [sd 8/13/98]

## Examples
```pascal
resultStr := CellString(1, 2);
```
```python
import vs

# Function CellString returns the string of a specified cell in the active
# worksheet.
row = 10
column = 5

text = vs.CellString(row, column)
vs.Message('CellString returned: ' + str(text))
```

## See Also
[IsWSCellString](IsWSCellString.md),  IsWSCellStringN, [IsWSSubrowCellString](IsWSSubrowCellString.md)

## Version
CellString is obsolete as of VectorWorks 9.0, see [IsWSCellString](IsWSCellString.md) (returns a string),  IsWSCellStringN (returns a Dynarray of Char), [IsWSSubrowCellString](IsWSSubrowCellString.md)

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
