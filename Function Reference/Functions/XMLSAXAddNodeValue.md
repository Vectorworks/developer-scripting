# XMLSAXAddNodeValue

## Description
Write XML using SAX, adds a node value to a node begun with [ XMLSAXBeginNode](XMLSAXBeginNode.md).

```pascal
FUNCTION XMLSAXAddNodeValue(
				XMLHandle : LONGINT;
				nodeValue : STRING): INTEGER;
```

```python
def vs.XMLSAXAddNodeValue(XMLHandle, nodeValue):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|nodeValue|STRING|   |

## Examples
[XMLSAXBeginDocFile](XMLSAXBeginDocFile.md) or [XMLSAXBeginDocMemory](XMLSAXBeginDocMemory.md).

## Version
Availability: from Vectorworks 2011

## Category
* [XML SAX](../Categories/XML%20SAX.md)
