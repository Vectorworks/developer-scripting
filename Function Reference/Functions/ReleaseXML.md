# ReleaseXML

## Description
Frees memory associated with the specified XMLHandle. Once this function is called, XMLHandle can no longer be used.

```pascal
FUNCTION ReleaseXML(XMLHandle : LONGINT):INTEGER;
```

```python
def vs.ReleaseXML(XMLHandle):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |

## Examples
[XMLParse](examples/XMLParse.md)

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
