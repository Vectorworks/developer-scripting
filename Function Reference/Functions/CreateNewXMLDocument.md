# CreateNewXMLDocument

## Description
Creates a new XML document root node. Returns an error code.

```pascal
FUNCTION CreateNewXMLDocument(
				XMLHandle       : LONGINT;
				rootElementName : STRING):INTEGER;
```

```python
def vs.CreateNewXMLDocument(XMLHandle, rootElementName):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|rootElementName|STRING|   |

## Examples
[WriteXMLFile](WriteXMLFile.md) and [WriteXMLMemory](WriteXMLMemory.md)

## See Also
[SetElementValue](SetElementValue.md) | [WriteXMLMemory](WriteXMLMemory.md) | [InitXML](InitXML.md) | [ReleaseXML](ReleaseXML.md)

## Version
Availability: from All Versions

## Category
* [XML](../Categories/XML.md)
