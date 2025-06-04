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

## Version
Availability: from Vectorworks 2020

## Category
* [Object Events](../Categories/Object%20Events.md)
