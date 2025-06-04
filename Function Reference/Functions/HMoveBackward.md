# HMoveBackward

## Description
Move the referenced object backward in the object stacking order. If toBack is TRUE, the object will be moved to the back of the stacking order.

```pascal
PROCEDURE HMoveBackward(
				h      : HANDLE;
				toBack : BOOLEAN);
```

```python
def vs.HMoveBackward(h, toBack):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|toBack|BOOLEAN|Move to back of stacking order.|

## Remarks
It is possible using HMoveForward and HMoveBackward to re-order layers. But use caution. Do not set the toBack argument to TRUE -- it will delete the layer. Also, Peter Vandewalle claims that the layer can get deleted even if toBack is FALSE, if you keep sending it backward. (I could not confirm this.)

## Version
Availability: from VectorWorks8.5

## Category
* [Object Editing](../Categories/Object%20Editing.md)
