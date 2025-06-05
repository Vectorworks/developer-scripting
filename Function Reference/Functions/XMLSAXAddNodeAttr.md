# XMLSAXAddNodeAttr

## Description
Write XML using SAX, adds a node attributes to a node begun with [ XMLSAXBeginNode](XMLSAXBeginNode.md).

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
[XMLSAXBeginDocFile](XMLSAXBeginDocFile.md) or [XMLSAXBeginDocMemory](XMLSAXBeginDocMemory.md).

## Version
Availability: from Vectorworks 2011

## Category
* [XML SAX](../Categories/XML%20SAX.md)
