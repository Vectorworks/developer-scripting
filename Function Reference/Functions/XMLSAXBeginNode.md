# XMLSAXBeginNode

## Description
Write XML using SAX, begin of a node. [[VS:XMLSAXEndNode| XMLSAXEndNode]] ends a node

```pascal
FUNCTION XMLSAXBeginNode(
				XMLHandle : LONGINT;
				nodeName  : STRING): INTEGER;
```

```python
def vs.XMLSAXBeginNode(XMLHandle, nodeName):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|nodeName|STRING|   |

## Examples
[[VS:XMLSAXBeginDocFile]] or [[VS:XMLSAXBeginDocMemory]].

## Version
Availability: from Vectorworks 2011

## Category
* [XML SAX](../Categories/XML%20SAX.md)
