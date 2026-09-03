# XMLSAXEndNode

## Description
Write XML using SAX, end of a node. [ XMLSAXBeginNode](XMLSAXBeginNode.md) begins a node.

```pascal
FUNCTION XMLSAXEndNode(XMLHandle : LONGINT): INTEGER;
```

```python
def vs.XMLSAXEndNode(XMLHandle):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |

## Examples
[XMLSAXBeginDocFile](XMLSAXBeginDocFile.md) or [XMLSAXBeginDocMemory](XMLSAXBeginDocMemory.md).

```pascal
resultN := XMLSAXEndNode(1);
```
```python
import vs

# Write XML using SAX, end of a node.
XMLHandle = 1

resultN = vs.XMLSAXEndNode(XMLHandle)
vs.Message('XMLSAXEndNode returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2011

## Category
* [XML SAX](../Categories/XML%20SAX.md)
