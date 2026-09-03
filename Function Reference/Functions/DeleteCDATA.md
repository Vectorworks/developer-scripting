# DeleteCDATA

## Description
Deletes the CDATA section of the specified element.  The parameter elementPath is specified as a path of element names.  Returns an error code.

```pascal
FUNCTION DeleteCDATA(
				XMLHandle   : LONGINT;
				elementPath : STRING):INTEGER;
```

```python
def vs.DeleteCDATA(XMLHandle, elementPath):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|elementPath|STRING|   |

## Examples
```pascal
resultN := DeleteCDATA(1, 'file.txt');
```
```python
import vs

# Deletes the CDATA section of the specified element.
XMLHandle = 1
elementPath = 'C:/Temp'

resultN = vs.DeleteCDATA(XMLHandle, elementPath)
vs.Message('DeleteCDATA returned: ' + str(resultN))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
