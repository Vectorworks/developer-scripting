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

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
