# GetNextElement

## Description
Gets the next element at the same XML nesting level.

```pascal
FUNCTION GetNextElement(
				XMLHandle   : LONGINT;
				elementPath : STRING;
				VAR value   : STRING):INTEGER;
```

```python
def vs.GetNextElement(XMLHandle, elementPath):
    return (INTEGER, value)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|elementPath|STRING|   |
|value|STRING|Output parameter.|

## Examples
```pascal
resultN := GetNextElement(1, 'file.txt', 'Example');
```
```python
import vs

# Gets the next element at the same XML nesting level.
XMLHandle = 1
elementPath = 'C:/Temp'

resultN, value = vs.GetNextElement(XMLHandle, elementPath)
vs.Message('GetNextElement returned: ' + str((resultN, value)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
