# vsoWidgetGetVisible

## Description
?

```pascal
FUNCTION vsoWidgetGetVisible(widgetID : LONGINT): BOOLEAN;
```

```python
def vs.vsoWidgetGetVisible(widgetID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |

## Examples
```pascal
resultOK := vsoWidgetGetVisible(1);
```
```python
import vs

# ?.
widgetID = 1

ok = vs.vsoWidgetGetVisible(widgetID)
if ok:
    vs.Message('vsoWidgetGetVisible succeeded')
else:
    vs.Message('vsoWidgetGetVisible failed')
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
