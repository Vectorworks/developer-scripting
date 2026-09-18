# XMLSAXAddNodeValue

## Description
Write XML using SAX, adds a node value to a node begun with [ XMLSAXBeginNode](XMLSAXBeginNode.md).

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
[XMLSAXBeginDocFile](XMLSAXBeginDocFile.md) or [XMLSAXBeginDocMemory](XMLSAXBeginDocMemory.md).

```pascal
resultN := XMLSAXAddNodeValue(1, 'Example');
```
```python
import vs

# Write XML using SAX, adds a node value to a node begun with XMLSAXBeginNode.
XMLHandle = 1
nodeValue = 'Example'

resultN = vs.XMLSAXAddNodeValue(XMLHandle, nodeValue)
vs.Message('XMLSAXAddNodeValue returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2011

## Category
* [XML SAX](../Categories/XML%20SAX.md)
