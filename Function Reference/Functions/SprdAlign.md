# SprdAlign

## Description
Procedure SprdAlign determines the alignment setting within a worksheet cell. 

**Table - Worksheet Cell Alignment**

| Alignment | Constant |
|-----------|----------|
| General   | 1        |
| Left      | 2        |
| Right     | 3        |
| Center    | 4        |

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
#### VectorScript ####
```pascal
SprdAlign(2);
LoadCell(3, 3, 'Cell 1, 1');
```
#### Python ####
```python

```

## See Also
[SetWSCellAlignment](SetWSCellAlignment.md)

## Version
SprdAlign is obsolete as of VectorWorks 9.0, see new [SetWSCellAlignment](SetWSCellAlignment.md).

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
