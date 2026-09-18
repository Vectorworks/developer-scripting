# CellHasNum

## Description
Function CellHasNum returns TRUE if the specified cell of a referenced worksheet contains a value or an equation which returns a numeric value.

```pascal
FUNCTION CellHasNum(
				h   : HANDLE;
				row : INTEGER;
				col : INTEGER): BOOLEAN;
```

```python
def vs.CellHasNum(h, row, col):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to worksheet.|
|row|INTEGER|Worksheet row index.|
|col|INTEGER|Worksheet column index.|

## Examples
```pascal
resultOK := CellHasNum(h, 1, 2);
```
```python
import vs

# Function CellHasNum returns TRUE if the specified cell of a referenced
# worksheet contains a value or an equation which returns a numeric value.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
row = 10
col = 5

ok = vs.CellHasNum(h, row, col)
if ok:
    vs.Message('CellHasNum succeeded')
else:
    vs.Message('CellHasNum failed')
```

## See Also
[IsWSCellNumber](IsWSCellNumber.md), [IsWSSubrowCellNumber](IsWSSubrowCellNumber.md)

## Version
CellHasNum is obsolete as of VectorWorks 9.0, see [IsWSCellNumber](IsWSCellNumber.md), [IsWSSubrowCellNumber](IsWSSubrowCellNumber.md)

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
