# XMLSAXEndDocMemory

## Description
Write XML using SAX, end of a document. [[VS:XMLSAXBeginDocMemory| XMLSAXBeginDocMemory]] begins a document.

```pascal
FUNCTION XMLSAXEndDocMemory(
				XMLHandle   : LONGINT;
				VAR XMLData : DYNARRAY[] of CHAR): INTEGER;
```

```python
def vs.XMLSAXEndDocMemory(XMLHandle):
    return (INTEGER, XMLData)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|XMLData|DYNARRAY[] of CHAR|   |

## Examples
[[VS:XMLSAXBeginDocMemory]].

## See Also
[InitXML](InitXML.md) | [ReleaseXML](ReleaseXML.md)

[XMLSAXBeginDocMemory](XMLSAXBeginDocMemory.md) | [XMLSAXBeginNode](XMLSAXBeginNode.md) | [XMLSAXEndNode](XMLSAXEndNode.md) | [XMLSAXAddNodeAttr](XMLSAXAddNodeAttr.md) | [XMLSAXAddNodeValue](XMLSAXAddNodeValue.md)

## Version
Availability: from Vectorworks 2011

## Category
* [XML SAX](../Categories/XML%20SAX.md)
