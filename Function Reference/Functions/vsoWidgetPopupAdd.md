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

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
