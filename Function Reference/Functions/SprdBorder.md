# SprdBorder

## Description
Procedure SprdBorder determines the border settings for cells within the active worksheet.

```pascal
PROCEDURE SprdBorder(
				top   : BOOLEAN;
				left  : BOOLEAN;
				bot   : BOOLEAN;
				right : BOOLEAN);
```

```python
def vs.SprdBorder(top, left, bot, right):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|top|BOOLEAN|Top border on-off setting.|
|left|BOOLEAN|Left border on-off setting.|
|bot|BOOLEAN|Bottom border on-off setting.|
|right|BOOLEAN|Right border on-off setting.|

## Examples
==== VectorScript ====
```pascal
SprdBorder(TRUE, FALSE, TRUE, FALSE);
LoadCell(1, 1, 'This is a string');
```
==== Python ====
```python

```

## See Also
[SetWSCellBorder| SetWSCellBorder](SetWSCellBorder|%20SetWSCellBorder.md)

## Version
SprdBorder is obsolete as of VectorWorks 9.0, see new [[VS:SetWSCellBorder| SetWSCellBorder]]

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
