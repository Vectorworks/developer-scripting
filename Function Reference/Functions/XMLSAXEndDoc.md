# XMLSAXEndDoc

## Description
Write XML using SAX, end of a document. [[VS:XMLSAXBeginDocFile| XMLSAXBeginDocFile]] begins a document.

```pascal
FUNCTION XMLSAXEndDoc(XMLHandle : LONGINT): INTEGER;
```

```python
def vs.XMLSAXEndDoc(XMLHandle):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |

## Examples
[[VS:XMLSAXBeginDocFile]].

## See Also
[InitXML](InitXML.md) | [ReleaseXML](ReleaseXML.md)

[XMLSAXBeginDocFile](XMLSAXBeginDocFile.md) | [XMLSAXBeginNode](XMLSAXBeginNode.md) | [XMLSAXEndNode](XMLSAXEndNode.md) | [XMLSAXAddNodeAttr](XMLSAXAddNodeAttr.md) | [XMLSAXAddNodeValue](XMLSAXAddNodeValue.md)

## Version
Availability: from Vectorworks 2011

## Category
* [XML SAX](../Categories/XML%20SAX.md)
