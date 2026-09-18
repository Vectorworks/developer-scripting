# vsoWidgetPopupGet

## Description
Get the text of an item from a popup widget. (For example, a dropdown list item of a PIO)

```pascal
PROCEDURE vsoWidgetPopupGet(
				widgetID    : LONGINT;
				index       : LONGINT;
				VAR outId   : STRING;
				VAR outText : STRING);
```

```python
def vs.vsoWidgetPopupGet(widgetID, index):
    return (outId, outText)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|The ID as shown in the 'Edit Plugin Definition' Dialog under Parameters->Column #|
|index|LONGINT|The 0-based index of the item|
|outId|STRING|Output parameter. The id of the item (if not overwritten, same as outText)|
|outText|STRING|Output parameter. The text of the item.|

## Examples
```pascal
vsoWidgetPopupGet(1, 2, 'Example', 'Example');
```
```python
import vs

# Get the text of an item from a popup widget.
widgetID = 1
index = 1

outId, outText = vs.vsoWidgetPopupGet(widgetID, index)
vs.Message('vsoWidgetPopupGet returned: ' + str((outId, outText)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
