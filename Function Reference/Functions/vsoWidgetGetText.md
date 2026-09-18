# vsoWidgetGetText

## Description
?

```pascal
FUNCTION vsoWidgetGetText(widgetID : LONGINT): STRING;
```

```python
def vs.vsoWidgetGetText(widgetID):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |

## Examples
```pascal
resultStr := vsoWidgetGetText(1);
```
```python
import vs

# ?.
widgetID = 1

text = vs.vsoWidgetGetText(widgetID)
vs.Message('vsoWidgetGetText returned: ' + str(text))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
