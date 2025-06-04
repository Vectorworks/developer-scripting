# GetElementValue

## Description
Returns the value of the element corresponding to the specified element name.  The parameter elementPath is specified as a path of element names. The return value is the error code (0 for no error, or non-0 if it failed). See [[VS:InitXML| InitXML]] for a list of the error codes.

The elementPath variable can be the explicit path, or you can use index notation to reference elements which all have the same xml tag:
 result := GetElementValue(hXML, '/geo/cloud/vector[2]/', str1);

```pascal
FUNCTION GetElementValue(
				XMLHandle   : LONGINT;
				elementPath : STRING;
				VAR value   : STRING):INTEGER;
```

```python
def vs.GetElementValue(XMLHandle, elementPath):
    return (INTEGER, value)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|elementPath|STRING|   |
|value|STRING|Output parameter.|

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
