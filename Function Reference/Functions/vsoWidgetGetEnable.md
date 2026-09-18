# vsoWidgetGetEnable

## Description
?

```pascal
FUNCTION vsoWidgetGetEnable(widgetID : LONGINT): BOOLEAN;
```

```python
def vs.vsoWidgetGetEnable(widgetID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |

## Examples
```pascal
resultOK := vsoWidgetGetEnable(1);
```
```python
import vs

# ?.
widgetID = 1

ok = vs.vsoWidgetGetEnable(widgetID)
if ok:
    vs.Message('vsoWidgetGetEnable succeeded')
else:
    vs.Message('vsoWidgetGetEnable failed')
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
