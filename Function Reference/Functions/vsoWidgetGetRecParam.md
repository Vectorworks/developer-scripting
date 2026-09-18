# vsoWidgetGetRecParam

## Description
Returns the fieldname from the plugin-definition by a widget id.
The opposite of [vsoPrmName2WidgetID](vsoPrmName2WidgetID.md)

```pascal
FUNCTION vsoWidgetGetRecParam(widgetID : LONGINT): STRING;
```

```python
def vs.vsoWidgetGetRecParam(widgetID):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |

## Examples
```pascal
resultStr := vsoWidgetGetRecParam(1);
```
```python
import vs

# Returns the fieldname from the plugin-definition by a widget id.
widgetID = 1

text = vs.vsoWidgetGetRecParam(widgetID)
vs.Message('vsoWidgetGetRecParam returned: ' + str(text))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
