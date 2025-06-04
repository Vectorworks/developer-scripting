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

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
