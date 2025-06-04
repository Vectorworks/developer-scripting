# GetFirstChild

## Description
Gets the last child within the specified element path. Use [[VS:GetPreviousElement| GetPreviousElement]] to step through the rest of the elements at the same nesting level.

```pascal
FUNCTION GetFirstChild(
				XMLHandle   : LONGINT;
				elementPath : STRING;
				VAR value   : STRING):INTEGER;
```

```python
def vs.GetFirstChild(XMLHandle, elementPath):
    return (INTEGER, value)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|elementPath|STRING|   |
|value|STRING|Output parameter.|

## Examples
LParse}}

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
