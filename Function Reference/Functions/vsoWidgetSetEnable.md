# vsoWidgetSetEnable

## Description
Sets whether or not the specified parameter is enabled on the Object Info Palette.

Note: This function should be called during the parametric OIP generation event: <code>41: {kObjOnWidgetPrep}</code>. See [[VS:Parametric Custom Shape Pane Popup]].

```pascal
PROCEDURE vsoWidgetSetEnable(
				widgetID : LONGINT;
				enabled  : BOOLEAN);
```

```python
def vs.vsoWidgetSetEnable(widgetID, enabled):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |
|enabled|BOOLEAN|   |

## Examples
```pascal
BEGIN
	vsoWidgetSetEnable( kDoorHandlesBtn, FALSE );
END;

BEGIN
	vsoWidgetSetVisible(8, FALSE);
	vsoWidgetSetVisible(9, FALSE);
	vsoWidgetSetEnable(5, (wallH <> NIL));
	vsoWidgetSetEnable(6, ((wallH <> NIL) & pSize_TO_Wall_Length));
	vsoWidgetSetEnable(7, ((wallH <> NIL) & pSize_to_Wall_Length));
	vsoSetEventResult( -8 {kObjectEventHandled} );
END;

BEGIN
	vsoWidgetSetEnable(DisplayIDWidgetID, TRUE);
END
```
```python
vs.vsoWidgetSetEnable( kWidgetID_NorthNo, 		vs.PNorth_Arrow )
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
