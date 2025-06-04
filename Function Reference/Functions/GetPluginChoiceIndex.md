# GetPluginChoiceIndex

## Description
Returns true with outIndex as specified by inPluginNameand inParameterName.  Each of the input names are universal names.

```pascal
FUNCTION GetPluginChoiceIndex(
				inPluginName    : STRING;
				inParameterName : STRING;
				inChoiceName    : STRING;
				VAR outIndex    : INTEGER): BOOLEAN;
```

```python
def vs.GetPluginChoiceIndex(inPluginName, inParameterName, inChoiceName):
    return (BOOLEAN, outIndex)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inPluginName|STRING|The universal name of the plug-in.|
|inParameterName|STRING|The universal name of the parameter.|
|inChoiceName|STRING|The universal name of the choice.|
|outIndex|INTEGER|The index of the requested choice.  ( range is 1 to n)|

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
