# DeleteAttribute

## Description
Deletes the attribute at the location specified by the path. Returns an error code.

```pascal
FUNCTION DeleteAttribute(
				XMLHandle   : LONGINT;
				elementPath : STRING;
				attribute   : STRING):INTEGER;
```

```python
def vs.DeleteAttribute(XMLHandle, elementPath, attribute):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|elementPath|STRING|   |
|attribute|STRING|   |

## Examples
```pascal
resultN := DeleteAttribute(1, 'file.txt', 'Example');
```
```python
import vs

# Deletes the attribute at the location specified by the path.
XMLHandle = 1
elementPath = 'C:/Temp'
attribute = 'Example'

resultN = vs.DeleteAttribute(XMLHandle, elementPath, attribute)
vs.Message('DeleteAttribute returned: ' + str(resultN))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
