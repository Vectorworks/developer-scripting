# vsoWidgetPopupGetTxt

## Description
For an OIP search popup widget, returns the text of an item specified by it's id.

```pascal
FUNCTION vsoWidgetPopupGetTxt(
				widgetID : LONGINT;
				id       : STRING): STRING;
```

```python
def vs.vsoWidgetPopupGetTxt(widgetID, id):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |
|id|STRING|   |

## Examples
```pascal
resultStr := vsoWidgetPopupGetTxt(1, 'Example');
```
```python
import vs

# For an OIP search popup widget, returns the text of an item specified by
# it's id.
widgetID = 1
id = 'Example'

text = vs.vsoWidgetPopupGetTxt(widgetID, id)
vs.Message('vsoWidgetPopupGetTxt returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2020

## Category
* [Object Events](../Categories/Object%20Events.md)
