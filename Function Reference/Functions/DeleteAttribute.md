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

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
