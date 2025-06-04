# GetPreviousElement

## Description
Gets the previous element in the same XML nesting level.

```pascal
FUNCTION GetPreviousElement(
				XMLHandle   : LONGINT;
				elementPath : STRING;
				VAR value   : STRING):INTEGER;
```

```python
def vs.GetPreviousElement(XMLHandle, elementPath):
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
