# SetObjPropTxtVS

## Description
Set a text value to an extended property.

```pascal
FUNCTION SetObjPropTxtVS(
				PropertyID  : LONGINT;
				PropertyVal : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.SetObjPropTxtVS(PropertyID, PropertyVal):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|PropertyID|LONGINT|   |
|PropertyVal|DYNARRAY[] of CHAR|   |

## Examples
```pascal
BEGIN
	gFlag := SetObjPropVS (		kObjXPropHasUIOverride,					TRUE);
	gFlag := SetObjPropVS (		kObjXHasCustomWidgetVisibilities,		TRUE);
	gFlag := SetObjPropCharVS(	kObjXPropUpdateAfterDocUnitsChange ,	Chr(kObjXPropResetMassForceDimChanged)	);
	gFlag := SetObjPropTxtVS(	kObjXPropAllowEquipmentItemAttach,		gPIOName								);
	gFlag := SetObjPropCharVS(	kWidgetGroupMode, 						Chr(kWidgetGroupAutomatic)				);
	gFlag := SetObjPropVS(		kObjXPropOipUnphased, 					TRUE									);
	gFlag := SetObjPropVS(		kObjXPropIsSymbolBased,					TRUE									);
	gFlag := vsoInsertAllParams;

BEGIN
	gFlag := SetObjPropVS (kObjXPropHasUIOverride,				TRUE);
	gFlag := SetObjPropVS (kObjXHasCustomWidgetVisibilities,	TRUE);
	gFlag := SetObjPropCharVS(	kObjXPropUpdateAfterDocUnitsChange ,	Chr(kObjXPropResetMassForceDimChanged)	);
	gFlag := SetObjPropTxtVS(	kObjXPropAllowEquipmentItemAttach,		gPIOName								);
	gFlag := SetObjPropCharVS(	kWidgetGroupMode, 					Chr(kWidgetGroupAutomatic)					);
	gFlag := SetObjPropVS(		kObjXPropOipUnphased, 				TRUE										);
	gFlag := vsoInsertAllParams;
```
```python
import vs

# Set a text value to an extended property.
PropertyID = 1
PropertyVal = 'Example'

ok = vs.SetObjPropTxtVS(PropertyID, PropertyVal)
if ok:
    vs.Message('SetObjPropTxtVS succeeded')
else:
    vs.Message('SetObjPropTxtVS failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [Object Events](../Categories/Object%20Events.md)
