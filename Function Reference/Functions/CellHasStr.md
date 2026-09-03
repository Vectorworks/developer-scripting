# CellHasStr

## Description
Function CellHasStr returns TRUE if the specified cell of a referenced worksheet contains a value or an equation which returns a string value.

```pascal
FUNCTION CellHasStr(
				h   : HANDLE;
				row : INTEGER;
				col : INTEGER): BOOLEAN;
```

```python
def vs.CellHasStr(h, row, col):
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
resultOK := CellHasStr(h, 1, 2);
```
```python
import vs

# Function CellHasStr returns TRUE if the specified cell of a referenced
# worksheet contains a value or an equation which returns a string value.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
row = 10
col = 5

ok = vs.CellHasStr(h, row, col)
if ok:
    vs.Message('CellHasStr succeeded')
else:
    vs.Message('CellHasStr failed')
```

## See Also
[IsWSCellString](IsWSCellString.md), [IsWSSubrowCellString](IsWSSubrowCellString.md)

## Version
CellHasStr is obsolete as of VectorWorks 9.0, see [IsWSCellString](IsWSCellString.md), [IsWSSubrowCellString](IsWSSubrowCellString.md)

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
