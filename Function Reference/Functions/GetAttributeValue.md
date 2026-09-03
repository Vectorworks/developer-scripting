# GetAttributeValue

## Description
Returns the value of the attribute corresponding to the specified element and attribute name.  The parameter elementPath is specified as a path of element names.  Returns attribute not found error if the attribute is not found.

```pascal
FUNCTION GetAttributeValue(
				XMLHandle   : LONGINT;
				elementPath : STRING;
				attribute   : STRING;
				VAR value   : STRING):INTEGER;
```

```python
def vs.GetAttributeValue(XMLHandle, elementPath, attribute):
    return (INTEGER, value)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|elementPath|STRING|   |
|attribute|STRING|   |
|value|STRING|Output parameter.|

## Examples
```pascal
BEGIN
	result := GetElementValue  (SourceIndex, Concat('/',xmlRootName,'/',xmlSpeakerFolder,'/',Concat(StkBxNum[ElementCount])), StkBxNum[ElementCount]);
	result := GetAttributeValue(SourceIndex, Concat('/',xmlRootName,'/',xmlSpeakerFolder,'/',Concat('Box',ElementCount)),
		'Brand', StkBxBrand[ElementCount]);
	result := GetAttributeValue(SourceIndex, Concat('/',xmlRootName,'/',xmlSpeakerFolder,'/',Concat('Box',ElementCount)),
		'Model', StkBxModel[ElementCount]);
	result := GetAttributeValue(SourceIndex, Concat('/',xmlRootName,'/',xmlSpeakerFolder,'/',Concat('Box',ElementCount)),
		'UserType', StkBxUsrType[ElementCount]);
```
```python
import vs

# Returns the value of the attribute corresponding to the specified element
# and attribute name.
XMLHandle = 1
elementPath = 'C:/Temp'
attribute = 'Example'

resultN, value = vs.GetAttributeValue(XMLHandle, elementPath, attribute)
vs.Message('GetAttributeValue returned: ' + str((resultN, value)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
