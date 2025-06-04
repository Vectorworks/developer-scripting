# vsoWidgetPopupSet

## Description
Sets the value of a choice in a popup widget. (For example, the item text of a dropdown list in a PIO)

```pascal
PROCEDURE vsoWidgetPopupSet(
				widgetID : LONGINT;
				index    : LONGINT;
				id       : STRING;
				text     : STRING);
```

```python
def vs.vsoWidgetPopupSet(widgetID, index, id, text):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|The ID as shown in the 'Edit Plugin Definition' Dialog under Parameters->Column #|
|index|LONGINT|The 0-based index of the item|
|id|STRING|The id of the item. (Can be the same as outText)|
|text|STRING|The text of the item|

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
