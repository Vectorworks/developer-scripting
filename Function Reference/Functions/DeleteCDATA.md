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

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
