# DeleteElement

## Description
Deletes the element at the location specified by the path.

```pascal
FUNCTION DeleteElement(
				XMLHandle   : LONGINT;
				elementPath : STRING):INTEGER;
```

```python
def vs.DeleteElement(XMLHandle, elementPath):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|elementPath|STRING|   |

## Examples
```pascal
BEGIN
	{delete the existing export field list}
	result := DeleteElement(hXML,Concat(xmlExpFlds));
END;

BEGIN
	result := SetElementValue  (hXML, Concat('/',xmlRootName,'/',xmlSpeakerFolder,'/',Concat('BoxTotal')), Concat(BxDataTtl-1));
	result := DeleteElement (hXML,Concat('/',xmlRootName,'/',xmlSpeakerFolder,'/',Concat('Box',MatchNumber)));
END
```
```python
import vs

# Deletes the element at the location specified by the path.
XMLHandle = 1
elementPath = 'C:/Temp'

resultN = vs.DeleteElement(XMLHandle, elementPath)
vs.Message('DeleteElement returned: ' + str(resultN))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
