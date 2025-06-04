# SetObjPropVS

## Description
See [[VS:Object Events]].

```pascal
FUNCTION SetObjPropVS(
				PropertyID  : LONGINT;
				PropertyVal : BOOLEAN):BOOLEAN;
```

```python
def vs.SetObjPropVS(PropertyID, PropertyVal):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|PropertyID|LONGINT|   |
|PropertyVal|BOOLEAN|   |

## Remarks
[Ptr 04/28/2020]
<code lang=py>
_bResult = vs.SetObjPropVS(2, True)  # kObjXPropHasLayerScaleDeps
_bResult = vs.SetObjPropVS(8, True)  # kObjXPropHasUIOverride
_bResult = vs.SetObjPropVS(18, True)  # kObjProp_AcceptStates
_bResult = vs.SetObjPropVS(49, True)  # kObjXSupportsStyles
_bResult = vs.SetObjPropVS(50, True)  # kObjXPropSupportGenericStoryLevel
_bResult = vs.SetObjPropVS(53, True)  # kObjXPropSupportResourcePopup
</code>

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
