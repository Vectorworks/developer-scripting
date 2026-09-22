# SetTopPlanVwCutPlane

## Description
Sets the Top/Plan view cut plane of a symbol definition, plug-in object style, or plug-in object.

```pascal
FUNCTION SetTopPlanVwCutPlane(
				hObject             : HANDLE;
				topPlanViewCutPlane : REAL (Coordinate)) : BOOLEAN;
```

```python
def vs.SetTopPlanVwCutPlane(hObject, topPlanViewCutPlane):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|
|topPlanViewCutPlane|REAL (Coordinate)|The Top/Plan view cut plane.|

## Returns
Whether the call succeeded.

## See Also
VS Functions:
[GetTopPlanVwCutPlane](GetTopPlanVwCutPlane.md)

## Version
Availability: from Vectorworks 2026.2

## Category
* [Objects - Custom](Categories/Objects%20-%20Custom.md)

