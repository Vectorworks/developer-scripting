# SetPlanarRef

## Description
Set the plane ref ID of the specified object.

```pascal
PROCEDURE SetPlanarRef(
				h     : HANDLE;
				refID : LONGINT);
```

```python
def vs.SetPlanarRef(h, refID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the object.|
|refID|LONGINT|Reference ID of the plane.|

## Remarks
The refID is the return value from [GetPlanarRef()](GetPlanarRef.md). As noted in [GetCurrentPlanarRefID()](GetCurrentPlanarRefID.md).
Screen Plane has a ref ID of 0.
Layer Plane has a ref ID of -1.

[[User:Rgm|Rgm]] [2012.05.16]:
Seems to be equivalent to SetObjectVariableBoolean(hd, 1160, TRUE);

In VW2011, this will silently fail to set an object to Screen Plane unless the object's Z is the negative of the Layer Z of the design layer the object exists on.

For example, if GetZVals(zVal, deltaZVal) gives a non-zero zVal, you'll have to call Move3DObj(hd, 0, 0, -zVal) before SetPlanarRef(hd,0) will have any effect.

## Version
Availability: from Vectorworks 2011

## Category
* [Object Info](../Categories/Object%20Info.md)
