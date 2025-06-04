# GetLocalizedPluginChoice

## Description
Returns true with outChoice as specified by inPluginName, inParameterName and inChoiceIndex.  Each of the input names are universal names.

```pascal
FUNCTION GetLocalizedPluginChoice(
				inPluginName    : STRING;
				inParameterName : STRING;
				inChoiceIndex   : INTEGER;
				VAR outChoice   : STRING): BOOLEAN;
```

```python
def vs.GetLocalizedPluginChoice(inPluginName, inParameterName, inChoiceIndex):
    return (BOOLEAN, outChoice)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inPluginName|STRING|The universal name of the plug-in.|
|inParameterName|STRING|The universal name of the parameter.|
|inChoiceIndex|INTEGER|The  index of the requested choice. ( range is 1 to n)|
|outChoice|STRING|The requested choice string.|

## See Also
VS Functions:
[GetLocalizedPluginName](GetLocalizedPluginName.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
