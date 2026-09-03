# XMLSAXBeginNode

## Description
Write XML using SAX, begin of a node. [ XMLSAXEndNode](XMLSAXEndNode.md) ends a node

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
[XMLSAXBeginDocFile](XMLSAXBeginDocFile.md) or [XMLSAXBeginDocMemory](XMLSAXBeginDocMemory.md).

```pascal
resultN := XMLSAXBeginNode(1, 'Example');
```
```python
import vs

# Write XML using SAX, begin of a node.
XMLHandle = 1
nodeName = 'Example'

resultN = vs.XMLSAXBeginNode(XMLHandle, nodeName)
vs.Message('XMLSAXBeginNode returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2011

## Category
* [XML SAX](../Categories/XML%20SAX.md)
