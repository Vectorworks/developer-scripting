# vsoWidgetSetType

## Description
Changes a type of a widget that was already added.

```pascal
PROCEDURE vsoWidgetSetType(
				widgetID   : LONGINT;
				widgetType : LONGINT);
```

```python
def vs.vsoWidgetSetType(widgetID, widgetType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |
|widgetType|LONGINT|   |

## Examples
```pascal
Result := SetObjPropVS (12,TRUE);	{kObjXHasCustomWidgetVisibilities}
bsb := vsoInsertAllParams;
bsb := vsoInsertWidget(1,kWidgetButton, kGrOptionsButton,GetPlugInString(5000), 0);
IF vsoPrmName2WidgetID('',kNNA_fLinkTo,kLinkToPopUp) THEN BEGIN
	vsoWidgetSetType( kLinkToPopUp, 108 {kWidgetSearchablePopup} );
	vsoWidgetPopupAddN(kLinkToPopUp,TRUE,'',GetPlugInString(5001), '','');
END;

bsb := vsoInsertWidget(1,kWidgetButton, kFlipButton,GetPlugInString(5000), 0);
bsb := vsoInsertWidget(2, kWidgetButton, kCreateButton, GetPlugInString(5006), 0);
bsb := vsoInsertWidget(3,kWidgetButton, kMarkerButton,GetPlugInString(5001), 0);
IF vsoPrmName2WidgetID('',kNNA_fLinkTo,kLinkToPopUp) THEN BEGIN
	vsoWidgetSetType( kLinkToPopUp, 108 {kWidgetSearchablePopup} );
	vsoWidgetPopupAddN(kLinkToPopUp,TRUE,'',GetPlugInString(5002),'','');
END;
```
```python
import vs

# Changes a type of a widget that was already added.
widgetID = 1
widgetType = 0

vs.vsoWidgetSetType(widgetID, widgetType)
```

## Version
Availability: from Vectorworks 2020

## Category
* [Object Events](../Categories/Object%20Events.md)
