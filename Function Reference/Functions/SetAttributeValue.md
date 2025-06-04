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

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
