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
```python
_bResult = vs.SetObjPropVS(2, True)  # kObjXPropHasLayerScaleDeps
_bResult = vs.SetObjPropVS(8, True)  # kObjXPropHasUIOverride
_bResult = vs.SetObjPropVS(18, True)  # kObjProp_AcceptStates
_bResult = vs.SetObjPropVS(49, True)  # kObjXSupportsStyles
_bResult = vs.SetObjPropVS(50, True)  # kObjXPropSupportGenericStoryLevel
_bResult = vs.SetObjPropVS(53, True)  # kObjXPropSupportResourcePopup
```

## Examples
```pascal
BEGIN
	bsb := SetObjPropVS(kObjXPropHasUIOverride, TRUE);
	bsb := SetObjPropVS(kObjXSupportsStyles, TRUE );
	bsb := SetObjPropVS(kObjXPropSupportResourcePopup, TRUE);
	bsb := SetObjPropVS(kObjXHasCustomWidgetVisibilities, TRUE );
	bsb := SetObjPropVS(kObjXPropCatalogSupport, TRUE);

BEGIN
	result := SetObjPropVS(kObjXPropHasUIOverride,     TRUE);
	result := SetObjPropVS(12 {kObjXHasCustomWidgetVisibilities}, TRUE);
	result := vsoInsertAllParams;
	SetPrefInt( 590, 1 ); {varParametricEnableStateEventing, kParametricStateEvent_ResetStatesEvent}
	result := SetObjPropVS(18, TRUE); {kObjXPropAcceptStates}

BEGIN
	result := SetObjPropVS(kObjXPropSupportResourcePopup, TRUE);
	result := SetObjPropVS(kObjXSupportsStyles, TRUE );
END;
```
```python
if theEvent == vs.kObjOnInitXProperties:
	# Enable custom shape pane
	ok = vs.SetObjPropVS( vs.kObjXPropHasLayerScaleDeps, True )
	ok = vs.SetObjPropVS( vs.kObjXPropTextStyleSupport, True )
	ok = vs.SetObjPropVS( vs.kObjXPropHasUIOverride, True )
	ok = vs.SetObjPropVS( vs.kObjXHasCustomWidgetVisibilities, True )

if theEvent == vs.kObjOnInitXProperties:
	# Enable custom shape pane
	vs.SetObjPropVS( vs.kObjXPropHasUIOverride, True )
	vs.SetObjPropVS( vs.kObjXHasCustomWidgetVisibilities, True )

if theEvent == vs.kObjOnInitXProperties:
	ok	= vs.SetObjPropVS( vs.kObjXPropHasUIOverride, True )
	ok	= vs.SetObjPropVS( vs.kObjXHasCustomWidgetVisibilities, True )
```
See also in tutorials: [Plug-in with widgets, basic example (Python)](../../Common/Tasks/Parametrics/Plug-in%20with%20widget%20basic%20example.md)

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
