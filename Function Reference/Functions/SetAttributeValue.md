# SetAttributeValue

## Description
Sets the value of the specified attribute of the specified element. The parameter elementPath is specified as a path of element names. Returns an error code.

```pascal
FUNCTION SetAttributeValue(
				XMLHandle   : LONGINT;
				elementPath : STRING;
				attribute   : STRING;
				value       : STRING):INTEGER;
```

```python
def vs.SetAttributeValue(XMLHandle, elementPath, attribute, value):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|elementPath|STRING|   |
|attribute|STRING|   |
|value|STRING|   |

## Examples
```pascal
result := SetElementValue  (TargetIndex, Concat('/',xmlRootName,'/',xmlSpeakerFolder,'/',Concat('Box',ElementCount)),
	Concat('Box',ElementCount));
result := SetAttributeValue(TargetIndex, Concat('/',xmlRootName,'/',xmlSpeakerFolder,'/',Concat('Box',ElementCount)),
	'Brand', Concat(StkBxBrand[ElementCount]));
result := SetAttributeValue(TargetIndex, Concat('/',xmlRootName,'/',xmlSpeakerFolder,'/',Concat('Box',ElementCount)),
	'Model', Concat(StkBxModel[ElementCount]));
	result := SetAttributeValue(TargetIndex, Concat('/',xmlRootName,'/',xmlSpeakerFolder,'/',Concat('Box',ElementCount)),
		'UserType', Concat(StkBxUsrType[ElementCount]));
```
```python
import vs

# Sets the value of the specified attribute of the specified element.
XMLHandle = 1
elementPath = 'C:/Temp'
attribute = 'Example'
value = 'Example'

resultN = vs.SetAttributeValue(XMLHandle, elementPath, attribute, value)
vs.Message('SetAttributeValue returned: ' + str(resultN))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
