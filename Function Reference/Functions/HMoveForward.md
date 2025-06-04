# HMoveForward

## Description
Move the referenced object forward in the object stacking order. If toFront is TRUE, the object will be moved to the front of the stacking order.

```pascal
PROCEDURE HMoveForward(
				h       : HANDLE;
				toFront : BOOLEAN);
```

```python
def vs.HMoveForward(h, toFront):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|toFront|BOOLEAN|Move object to front of stacking order.|

## Remarks
It is possible using HMoveForward and HMoveBackward to re-order layers. But use caution. Do not set the toFront argument to TRUE -- it will delete the layer. Also, Peter Vandewalle claims that the layer can get deleted even if toFront is FALSE, if you keep sending it backward. (I could not confirm this.)

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
BEGIN
HMoveForward(FSActLayer, FALSE);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	vs.HMoveForward(vs.FSActLayer(), False)

Example()
```

## Version
Availability: from VectorWorks8.5

## Category
* [Object Editing](../Categories/Object%20Editing.md)
