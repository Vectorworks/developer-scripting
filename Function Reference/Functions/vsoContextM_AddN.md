# vsoContextM_AddN

## Description
Add an item to the context menu of the object during ObjectContextMenuEvent::kAction_Init event.

```pascal
PROCEDURE vsoContextM_AddN(
				locName : STRING;
				itemID  : INTEGER;
				helpID  : STRING;
				helpStr : STRING);
```

```python
def vs.vsoContextM_AddN(locName, itemID, helpID, helpStr):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|locName|STRING|   |
|itemID|INTEGER|   |
|helpID|STRING|   |
|helpStr|STRING|   |

## Examples
```pascal
BEGIN
	vsoContextM_AddN( GetPlugInString(3002), 1, 'SelectFocusedLightingDevices', GetPlugInString(3004) );
END;

BEGIN
	vsoContextM_AddN(GetPluginString(7001) , 1, 'SelectHoistsOrigin', GetPluginString(7002) );
END;

BEGIN
	vsoContextM_AddN( GetPluginString(4002) , 1,'AssigntoSelectedHoists', GetPluginString(4004));
	vsoContextM_AddN( GetPluginString(4003) , 2,'SelectOriginsHoists', GetPluginString(4005) );
END;
```
```python
import vs

# Add an item to the context menu of the object during
# ObjectContextMenuEvent::kAction_Init event.
locName = 'Example'
itemID = 1
helpID = 'Example'
helpStr = 'Example'

vs.vsoContextM_AddN(locName, itemID, helpID, helpStr)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Object Events](../Categories/Object%20Events.md)
