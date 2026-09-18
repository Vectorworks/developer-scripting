# DSelectAll

## Description
Procedure DSelectAll deselects all selected visible objects on the active layer of a VectorWorks document. If Layer Options is set to Show-Snap-Modify Others, then DSelectAll will deselect all selected visible objects within the document.

```pascal
PROCEDURE DSelectAll;
```

```python
def vs.DSelectAll():
    return None
```

## Examples
```pascal
DSelectAll;
```
```python
vs.MoveTo ( textPtx, textPty )
vs.DSelectAll()
vs.CreateText( vs.PSheet_No )
vs.SetFPat( vs.LNewObj(), 0 )
vs.Rotate( dTextRotation )

vs.Rotate( sweepTmp - 90 )
hObj = vs.LNewObj()
vs.DSelectAll()

vs.DSelectAll()
```

## Version
Availability: from All Versions

## Category
* [Selection](../Categories/Selection.md)
