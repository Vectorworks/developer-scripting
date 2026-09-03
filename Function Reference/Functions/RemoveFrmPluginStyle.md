# RemoveFrmPluginStyle

## Description
Removes an entry from the plug-in style map.

```pascal
FUNCTION RemoveFrmPluginStyle(
				hSymDef  : HANDLE;
				itemName : STRING): BOOLEAN;
```

```python
def vs.RemoveFrmPluginStyle(hSymDef, itemName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hSymDef|HANDLE|Handle to symbol definition containing a plug-in style.|
|itemName|STRING|Name of the item to remove from the plug-in style.|

## Examples
```pascal
IF RemoveFrmPluginStyle(hSymDef, 	'ActSolSpace'		) THEN BEGIN END;
IF RemoveFrmPluginStyle(hSymDef, 	'TtlSolenoids'		) THEN BEGIN END;
IF RemoveFrmPluginStyle(hSymDef, 	'ActSegLngth'		) THEN BEGIN END;
IF RemoveFrmPluginStyle(hSymDef, 	'ActSegCount'		) THEN BEGIN END;
IF RemoveFrmPluginStyle(hSymDef, 	'TTLSGLngth'		) THEN BEGIN END;
```
```python
import vs

# Removes an entry from the plug-in style map.
hSymDef = vs.GetObject('MySymbol')  # handle to a symbol definition
itemName = 'Example'

ok = vs.RemoveFrmPluginStyle(hSymDef, itemName)
if ok:
    vs.Message('RemoveFrmPluginStyle succeeded')
else:
    vs.Message('RemoveFrmPluginStyle failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
