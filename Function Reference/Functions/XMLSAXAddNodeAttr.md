# XMLSAXAddNodeAttr

## Description
Write XML using SAX, adds a node attributes to a node begun with [[VS:XMLSAXBeginNode| XMLSAXBeginNode]].

```pascal
FUNCTION XMLSAXAddNodeAttr(
				XMLHandle     : LONGINT;
				nodeAttrName  : STRING;
				nodeAttrValue : STRING): INTEGER;
```

```python
def vs.XMLSAXAddNodeAttr(XMLHandle, nodeAttrName, nodeAttrValue):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|nodeAttrName|STRING|   |
|nodeAttrValue|STRING|   |

## Examples
[[VS:XMLSAXBeginDocFile]] or [[VS:XMLSAXBeginDocMemory]].

## Version
Availability: from Vectorworks 2011

## Category
* [XML SAX](../Categories/XML%20SAX.md)
