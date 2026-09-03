# XMLSAXEndDoc

## Description
Write XML using SAX, end of a document. [ XMLSAXBeginDocFile](XMLSAXBeginDocFile.md) begins a document.

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
[XMLSAXBeginDocFile](XMLSAXBeginDocFile.md).

```pascal
resultN := XMLSAXEndDoc(1);
```
```python
import vs

# Write XML using SAX, end of a document.
XMLHandle = 1

resultN = vs.XMLSAXEndDoc(XMLHandle)
vs.Message('XMLSAXEndDoc returned: ' + str(resultN))
```

## See Also
[InitXML](InitXML.md) | [ReleaseXML](ReleaseXML.md)

[XMLSAXBeginDocFile](XMLSAXBeginDocFile.md) | [XMLSAXBeginNode](XMLSAXBeginNode.md) | [XMLSAXEndNode](XMLSAXEndNode.md) | [XMLSAXAddNodeAttr](XMLSAXAddNodeAttr.md) | [XMLSAXAddNodeValue](XMLSAXAddNodeValue.md)

## Version
Availability: from Vectorworks 2011

## Category
* [XML SAX](../Categories/XML%20SAX.md)
