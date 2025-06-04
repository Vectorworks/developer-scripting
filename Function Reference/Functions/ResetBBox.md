# ResetBBox

## Description
Procedure ResetBBox forces the bounding box information for the specified object to be recomputed based on the objects' current geometry. 

Call this procedure after modifying an object to force a redraw of the object.

```pascal
PROCEDURE ResetBBox(h : HANDLE);
```

```python
def vs.ResetBBox(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Forces the bouding box information for object h to be recomputed based on current geometry.

This doesn't seem to work on symdefs.

## Version
Availability: from All Versions

## Category
* [Object Editing](../Categories/Object%20Editing.md)
