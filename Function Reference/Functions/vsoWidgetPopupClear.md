# vsoWidgetPopupClear

## Description
Removes all items / choices of the specified popup widget

```pascal
PROCEDURE vsoWidgetPopupClear(widgetID : LONGINT);
```

```python
def vs.vsoWidgetPopupClear(widgetID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |

## Examples
```pascal
BSB := vsoPrmName2WidgetID( '', 'Door Config', gDoorSwingID );
vsoWidgetPopupClear( gDoorSwingID );
vsoWidgetPopupClear( gDoorSwingID );

vsoWidgetPopupClear(6);

IF vsoPrmName2WidgetID('',kNNA_fLinkTo,kLinkToPopUp) THEN
	vsoWidgetPopupClear(kLinkToPopUp);
ALLOCATE VPData [1..500];
NumVPs := 0;
ForEachObjectInLayer(BuildVPList,0,1,1);
SortArray(VPData,NumVPs,1);
```
```python
import vs

# Removes all items / choices of the specified popup widget.
widgetID = 1

vs.vsoWidgetPopupClear(widgetID)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
