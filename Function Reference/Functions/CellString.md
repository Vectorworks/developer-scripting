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

## See Also
[IsWSCellString | IsWSCellString](IsWSCellString%20| IsWSCellString.md),  [IsWSCellStringN | IsWSCellStringN](IsWSCellStringN%20| IsWSCellStringN.md), [IsWSSubrowCellString | IsWSSubrowCellString](IsWSSubrowCellString%20| IsWSSubrowCellString.md)

## Version
CellString is obsolete as of VectorWorks 9.0, see [[VS:IsWSCellString | IsWSCellString]] (returns a string),  [[VS:IsWSCellStringN | IsWSCellStringN]] (returns a Dynarray of Char), [[VS:IsWSSubrowCellString | IsWSSubrowCellString]]

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
