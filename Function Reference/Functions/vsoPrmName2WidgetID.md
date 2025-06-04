# vsoPrmName2WidgetID

## Description
Retrieves the widget id of a field from the plugin-definition by name.
The opposite of [[VS:vsoWidgetGetRecParam|vsoWidgetGetRecParam]]

```pascal
FUNCTION vsoPrmName2WidgetID(
				recName         : STRING;
				paramName       : STRING;
				VAR outWidgetID : LONGINT): BOOLEAN;
```

```python
def vs.vsoPrmName2WidgetID(recName, paramName):
    return (BOOLEAN, outWidgetID)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|recName|STRING|   |
|paramName|STRING|   |
|outWidgetID|LONGINT|   |

## Remarks
For this function to work, you need to use an empty string for the record name.

## Version
Availability: from Vectorworks 2011

## Category
* [Object Events](../Categories/Object%20Events.md)
