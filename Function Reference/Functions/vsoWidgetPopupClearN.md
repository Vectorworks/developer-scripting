# vsoWidgetPopupClearN

## Description
For an OIP search popup widget, clears the static or dynamic choices.

```pascal
PROCEDURE vsoWidgetPopupClearN(
				widgetID      : LONGINT;
				staticChoices : BOOLEAN);
```

```python
def vs.vsoWidgetPopupClearN(widgetID, staticChoices):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |
|staticChoices|BOOLEAN|   |

## Examples
```pascal
vsoWidgetPopupClearN(1, TRUE);
```
```python
import vs

# For an OIP search popup widget, clears the static or dynamic choices.
widgetID = 1
staticChoices = True

vs.vsoWidgetPopupClearN(widgetID, staticChoices)
```

## Version
Availability: from Vectorworks 2020

## Category
* [Object Events](../Categories/Object%20Events.md)
