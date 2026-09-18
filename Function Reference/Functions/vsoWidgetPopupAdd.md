# vsoWidgetPopupAdd

## Description
Adds an item to the widget choices.

```pascal
PROCEDURE vsoWidgetPopupAdd(
				widgetID : LONGINT;
				id       : STRING;
				text     : STRING);
```

```python
def vs.vsoWidgetPopupAdd(widgetID, id, text):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |
|id|STRING The value that is written into the database field when the related text is selected.|   |
|text|STRING This value is displayed in the PopUp.|   |

## Remarks
The PopUp is easy to handle if you use the same value for id and text. So that the display text is equal to the database value.

## Examples
```pascal
vsoWidgetPopupAdd( gDoorSwingID, kDoorConfigLeft,  GetPluginString(3008));
vsoWidgetPopupAdd( gDoorSwingID, kDoorConfigRight, GetPluginString(3009));
IF ( pStyle = kBCStrCorSq ) | (pStyle = kBCStrCorDiag)
| (pStyle = kBCStrStandard) | (pStyle = kBCStrSinkFront)  THEN
BEGIN

IF ( Len(optShort) > 0 ) THEN
	vsoWidgetPopupAdd(6, kShort, optShort);
IF ( Len(optMedium) > 0 ) THEN
	vsoWidgetPopupAdd(6, kMedium, optMedium);
IF ( Len(optLong) > 0 ) THEN
	vsoWidgetPopupAdd(6, kLong, optLong);

NumVPs := 0;
ForEachObjectInLayer(BuildVPList,0,1,1);
SortArray(VPData,NumVPs,1);
For I := 1 to NumVPs DO
	vsoWidgetPopupAdd(kLinkToPopUp,VPData[I].VPName,VPData[I].VPNumTitle);
vsoSetEventResult (-8);
Setup;
END;
```
```python
import vs

# Adds an item to the widget choices.
widgetID = 1
id = 'Example'
text = 'Example text'

vs.vsoWidgetPopupAdd(widgetID, id, text)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
