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

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
