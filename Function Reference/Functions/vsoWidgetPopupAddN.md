# vsoWidgetPopupAddN

## Description
Add an item to an OIP search popup widget. Static item is fixed at the top of the list, unsearchable. Non static items are searchable displayed in a list.

```pascal
PROCEDURE vsoWidgetPopupAddN(
				widgetID       : LONGINT;
				isStaticChoice : BOOLEAN;
				id             : STRING;
				text           : STRING;
				toolTip        : STRING;
				iconSpec       : STRING);
```

```python
def vs.vsoWidgetPopupAddN(widgetID, isStaticChoice, id, text, toolTip, iconSpec):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |
|isStaticChoice|BOOLEAN|   |
|id|STRING|   |
|text|STRING|   |
|toolTip|STRING|   |
|iconSpec|STRING|   |

## Examples
```pascal
bsb := vsoInsertAllParams;
bsb := vsoInsertWidget(1,kWidgetButton, kGrOptionsButton,GetPlugInString(5000), 0);
IF vsoPrmName2WidgetID('',kNNA_fLinkTo,kLinkToPopUp) THEN BEGIN
	vsoWidgetSetType( kLinkToPopUp, 108 {kWidgetSearchablePopup} );
	vsoWidgetPopupAddN(kLinkToPopUp,TRUE,'',GetPlugInString(5001), '','');
END;

bsb := vsoInsertWidget(2, kWidgetButton, kCreateButton, GetPlugInString(5006), 0);
bsb := vsoInsertWidget(3,kWidgetButton, kMarkerButton,GetPlugInString(5001), 0);
IF vsoPrmName2WidgetID('',kNNA_fLinkTo,kLinkToPopUp) THEN BEGIN
	vsoWidgetSetType( kLinkToPopUp, 108 {kWidgetSearchablePopup} );
	vsoWidgetPopupAddN(kLinkToPopUp,TRUE,'',GetPlugInString(5002),'','');
END;
```
```python
import vs

# Add an item to an OIP search popup widget.
widgetID = 1
isStaticChoice = True
id = 'Example'
text = 'Example text'
toolTip = 'Example'
iconSpec = 'Example'

vs.vsoWidgetPopupAddN(widgetID, isStaticChoice, id, text, toolTip, iconSpec)
```

## Version
Availability: from Vectorworks 2020

## Category
* [Object Events](../Categories/Object%20Events.md)
