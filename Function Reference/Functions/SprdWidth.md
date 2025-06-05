# SprdWidth

## Description
Procedure SprdWidth specifies the width of cells in a worksheet when loaded.

```pascal
PROCEDURE SprdWidth(width : REAL);
```

```python
def vs.SprdWidth(width):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|width|REAL|Width of worksheet cell (0-255 characters).|

## Examples
#### VectorScript ####
```pascal
SprdWidth(7);
LoadCell(1,1,'Cell 1,1');
```
#### Python ####
```python

```

## See Also
[SetWSColumnWidth](SetWSColumnWidth.md)

## Version
SprdWidth is obsolete as of VectorWorks 9.0, see new [ SetWSColumnWidth](SetWSColumnWidth.md)

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
