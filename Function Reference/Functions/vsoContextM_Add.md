# vsoContextM_Add

## Description
Add an item to the context menu of the object during kObjOnContextMenuInit event.

```pascal
PROCEDURE vsoContextM_Add(
				locName : STRING;
				itemID  : INTEGER;
				helpID  : STRING);
```

```python
def vs.vsoContextM_Add(locName, itemID, helpID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|locName|STRING|   |
|itemID|INTEGER|   |
|helpID|STRING|   |

## Examples
```pascal
BEGIN
	vsoContextM_Add( GetPluginString(3000) , 1, 'cm_Select_Multicable' );
	{vsoContextM_Add( GetPluginString(3001) , 2, '' );	}
END;
```
```python
import vs

# Add an item to the context menu of the object during kObjOnContextMenuInit
# event.
locName = 'Example'
itemID = 1
helpID = 'Example'

vs.vsoContextM_Add(locName, itemID, helpID)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Object Events](../Categories/Object%20Events.md)
