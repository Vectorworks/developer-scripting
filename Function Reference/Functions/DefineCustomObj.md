# DefineCustomObj

## Description
Calls GS_DefineCustomObject for a passed plugin name and preference.

```pascal
FUNCTION DefineCustomObj(
				pluginName : STRING;
				prefWhen   : INTEGER): HANDLE;
```

```python
def vs.DefineCustomObj(pluginName, prefWhen):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pluginName|STRING|The name of the plug-in for which preferences to be shown.|
|prefWhen|INTEGER|When the preference dialog is to be shown. See remarks for details.|

## Remarks
The parameter '''prefWhen''' can be one of:
* kCustomObjectPrefNever 	= 0
* kCustomObjectPrefAlways 	= 1
* kCustomObjectPrefNew 		= 2

([[User:CBM-c-|_c_]], 2016.02.08): 
Objects created with this call won't allow you to set a profile group, even if they usually support it.

## Version
Availability: from Vectorworks 2014

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
