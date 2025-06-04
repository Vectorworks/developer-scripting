# EnableParameter

## Description
For plug-in objects, this procedure sets whether or not the specified parameter is enabled on the Object Info Palette.  This routine is used inside plug-in object regeneration scripts to set their parameter enable state.  This state is an object instance property.

```pascal
PROCEDURE EnableParameter(
				inPlugin        : HANDLE;
				inParameterName : STRING;
				inSetEnabled    : BOOLEAN);
```

```python
def vs.EnableParameter(inPlugin, inParameterName, inSetEnabled):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inPlugin|HANDLE|Handle to the currently executing plug-in object.|
|inParameterName|STRING|Name of parameter, as it appears in the plug-in editor's parameter list.|
|inSetEnabled|BOOLEAN|Enabling flag.|

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
