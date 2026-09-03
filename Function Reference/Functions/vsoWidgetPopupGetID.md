# vsoWidgetPopupGetID

## Description
For an OIP search popup widget, returns the IDName for an item specified by it's text.

```pascal
FUNCTION vsoWidgetPopupGetID(
				widgetID : LONGINT;
				text     : STRING): STRING;
```

```python
def vs.vsoWidgetPopupGetID(widgetID, text):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |
|text|STRING|   |

## Examples
```pascal
resultStr := vsoWidgetPopupGetID(1, 'Example');
```
```python
import vs

# For an OIP search popup widget, returns the IDName for an item specified by
# it's text.
widgetID = 1
text = 'Example text'

text = vs.vsoWidgetPopupGetID(widgetID, text)
vs.Message('vsoWidgetPopupGetID returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2020

## Category
* [Object Events](../Categories/Object%20Events.md)
