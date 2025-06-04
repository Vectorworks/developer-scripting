# XMLSAXAddNodeValue

## Description
Write XML using SAX, adds a node value to a node begun with [[VS:XMLSAXBeginNode| XMLSAXBeginNode]].

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
[[VS:XMLSAXBeginDocFile]] or [[VS:XMLSAXBeginDocMemory]].

## Version
Availability: from Vectorworks 2011

## Category
* [XML SAX](../Categories/XML%20SAX.md)
