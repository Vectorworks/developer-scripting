# SetUseWallCutPlane

## Description
Sets the use wall cut plane setting of a symbol definition, plug-in object style, or plug-in object.

```pascal
FUNCTION SetUseWallCutPlane(
				hObject         : HANDLE;
				useWallCutPlane : BOOLEAN) : BOOLEAN;
```

```python
def vs.SetUseWallCutPlane(hObject, useWallCutPlane):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|
|useWallCutPlane|BOOLEAN|The use wall cut plane setting.|

## Returns
Whether the call succeeded.

## See Also
VS Functions:
[GetUseWallCutPlane](GetUseWallCutPlane.md)

## Version
Availability: from Vectorworks 2026.2

## Category
* [Objects - Custom](Categories/Objects%20-%20Custom.md)

