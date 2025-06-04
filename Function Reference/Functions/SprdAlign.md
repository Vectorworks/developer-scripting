# SprdAlign

## Description
Procedure SprdAlign determines the alignment setting within a worksheet cell. 

{| class="wikitable_c"
|+ Table - Worksheet Cell Alignment
! Alignment !! Constant
|- 
| General
| style="text-align:center"| 1
|- 
| Left
| style="text-align:center"| 2
|- 
| Right
| style="text-align:center"| 3
|- 
| Center
| style="text-align:center"| 4
|}

```pascal
PROCEDURE SprdAlign(align : INTEGER);
```

```python
def vs.SprdAlign(align):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|align|INTEGER|Text alignment within worksheet cell.|

## Examples
==== VectorScript ====
```pascal
SprdAlign(2);
LoadCell(3, 3, 'Cell 1, 1');
```
==== Python ====
```python

```

## See Also
[SetWSCellAlignment| SetWSCellAlignment](SetWSCellAlignment|%20SetWSCellAlignment.md)

## Version
SprdAlign is obsolete as of VectorWorks 9.0, see new [[VS:SetWSCellAlignment| SetWSCellAlignment]].

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
