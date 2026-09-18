# XMLSAXEndDocMemory

## Description
Write XML using SAX, end of a document. [ XMLSAXBeginDocMemory](XMLSAXBeginDocMemory.md) begins a document.

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
[XMLSAXBeginDocMemory](XMLSAXBeginDocMemory.md).

```pascal
resultN := XMLSAXEndDocMemory(1, XMLData);
```
```python
import vs

# Write XML using SAX, end of a document.
XMLHandle = 1

resultN, XMLData = vs.XMLSAXEndDocMemory(XMLHandle)
vs.Message('XMLSAXEndDocMemory returned: ' + str((resultN, XMLData)))
```

## See Also
[InitXML](InitXML.md) | [ReleaseXML](ReleaseXML.md)

[XMLSAXBeginDocMemory](XMLSAXBeginDocMemory.md) | [XMLSAXBeginNode](XMLSAXBeginNode.md) | [XMLSAXEndNode](XMLSAXEndNode.md) | [XMLSAXAddNodeAttr](XMLSAXAddNodeAttr.md) | [XMLSAXAddNodeValue](XMLSAXAddNodeValue.md)

## Version
Availability: from Vectorworks 2011

## Category
* [XML SAX](../Categories/XML%20SAX.md)
