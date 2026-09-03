# vsoWidgetSetVisible

## Description
Sets whether or not the specified parameter is visible on the Object Info Palette.

Note: This function should be called during the parametric OIP generation event: <code>41: {kObjOnWidgetPrep}</code>. See [[VS:Parametric Custom Shape Pane Popup]].

```pascal
PROCEDURE vsoWidgetSetVisible(
				widgetID : LONGINT;
				visible  : BOOLEAN);
```

```python
def vs.vsoWidgetSetVisible(widgetID, visible):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |
|visible|BOOLEAN|   |

## Examples
```pascal
BEGIN
	bsb := vsoPrmName2WidgetID( '', 'Door Swing', widgetID );
	vsoWidgetSetVisible( widgetID, FALSE );
	bsb := vsoPrmName2WidgetID( '', 'Number of Doors', widgetID );
	vsoWidgetSetVisible( widgetID, FALSE );
	bsb := vsoPrmName2WidgetID( '', 'PrevStyle', widgetID );
	vsoWidgetSetVisible( widgetID, FALSE );

BEGIN
	vsoWidgetSetVisible(8, FALSE);
	vsoWidgetSetVisible(9, FALSE);
	vsoWidgetSetEnable(5, (wallH <> NIL));
	vsoWidgetSetEnable(6, ((wallH <> NIL) & pSize_TO_Wall_Length));
	vsoWidgetSetEnable(7, ((wallH <> NIL) & pSize_to_Wall_Length));

result := vsoPrmName2WidgetID( '', '__boltType_inch', displayIDWidgetID );
vsoWidgetSetVisible( displayIDWidgetID, gSeries = 1 );
result := vsoPrmName2WidgetID( '', '__boltType_metric', displayIDWidgetID );
vsoWidgetSetVisible( displayIDWidgetID, gSeries = 2 );
```
```python
def UpdateParametersState():
	vs.vsoWidgetSetVisible( kWidgetID_UseGradeLimits, vs.PShow_Fences )

def UpdateParametersState():
	vs.vsoWidgetSetVisible( kWidgetID_UseGradeLimits, vs.PUse_Site_Modifiers )

elif theEvent == vs.kObjOnWidgetPrep:
	vs.vsoWidgetSetVisible( kWidget_UseGradeLimits, vs.PShow_Fences )
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
