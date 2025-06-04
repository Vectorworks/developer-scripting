# LoadCell

## Description
Procedure LoadCell inserts a value into a specified cell of the active worksheet.

```pascal
PROCEDURE LoadCell(
				row   : INTEGER;
				col   : INTEGER;
				entry : STRING);
```

```python
def vs.LoadCell(ro, col, entry):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|row|INTEGER|Worksheet row index.|
|col|INTEGER|Worksheet column index.|
|entry|STRING|Worksheet entry value.|

## Examples
#### VectorScript ####
```pascal
SprdSheet(0, 0, 3, 3);
LoadCell(1, 1, '= (14 + 2) * 3');
{ inserts a formula into a cell }

SprdSheet(0, 0, 3, 3);
LoadCell(1, 1, 'Window Schedule');
{ inserts a literal into a cell }
```
#### Python ####
```python

```

## See Also
VS functions:
* [SetWSCellFormula| SetWSCellFormula](SetWSCellFormula|%20SetWSCellFormula.md) (string, obsolete from VW 2012)
* [SetWSCellFormulaN| SetWSCellFormulaN](SetWSCellFormulaN|%20SetWSCellFormulaN.md) (Dynarray of Char)

## Version
LoadCell is obsolete as of VectorWorks 9.0, see new [[VS:SetWSCellFormula| SetWSCellFormula]] (string),  [[VS:SetWSCellFormulaN| SetWSCellFormulaN]] (Dynarray of Char).

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
