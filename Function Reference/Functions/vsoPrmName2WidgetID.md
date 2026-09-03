# vsoPrmName2WidgetID

## Description
Retrieves the widget id of a field from the plugin-definition by name.
The opposite of [vsoWidgetGetRecParam](vsoWidgetGetRecParam.md)

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

## Examples
```pascal
BSB := vsoPrmName2WidgetID( '', 'Door Config', gDoorSwingID );
vsoWidgetPopupClear( gDoorSwingID );
vsoWidgetPopupClear( gDoorSwingID );

result := vsoPrmName2WidgetID( '', '__boltType_inch', displayIDWidgetID );
vsoWidgetSetVisible( displayIDWidgetID, gSeries = 1 );
result := vsoPrmName2WidgetID( '', '__boltType_metric', displayIDWidgetID );
vsoWidgetSetVisible( displayIDWidgetID, gSeries = 2 );

BEGIN
	result := vsoPrmName2WidgetID( '', widgetName, widgetID );
	vsoWidgetSetVisible( widgetID, visible );
END;
```
```python
import vs

# Retrieves the widget id of a field from the plugin-definition by name.
recName = 'Example'
paramName = 'Example'

ok, outWidgetID = vs.vsoPrmName2WidgetID(recName, paramName)
vs.Message('vsoPrmName2WidgetID returned: ' + str((ok, outWidgetID)))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Object Events](../Categories/Object%20Events.md)
