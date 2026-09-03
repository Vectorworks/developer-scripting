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

```pascal
BEGIN
	xmlID := InitXML;
	IF ReadXMLFile(xmlID, -1, PlugInsCommonDataPreferences) <> 0 THEN int := CreateNewXMLDocument(xmlID, 'Preferences');
END;

 	BEGIN
 		xmlExpFlds := Concat('/',kSLDataFileTag,'/',kxmlExportFields);
UseDefaultFileErrorHandling(FALSE);
IF ReadXMLFile(hXML, -1, xmlFileNpath) <> 0 THEN
    result := CreateNewXMLDocument(hXML,kSLDataFileTag);
result := FindElement(hXML,Concat('/',kSLDataFileTag),kxmlExportFields,str);
IF result = 0 THEN
BEGIN
	{delete the existing export field list}

BEGIN
	result := CreateNewXMLDocument(hXML, Concat(xmlRootName));
```
```python
import vs

# Creates a new XML document root node.
XMLHandle = 1
rootElementName = 'Example'

resultN = vs.CreateNewXMLDocument(XMLHandle, rootElementName)
vs.Message('CreateNewXMLDocument returned: ' + str(resultN))
```

## See Also
[SetElementValue](SetElementValue.md) | [WriteXMLMemory](WriteXMLMemory.md) | [InitXML](InitXML.md) | [ReleaseXML](ReleaseXML.md)

## Version
Availability: from All Versions

## Category
* [XML](../Categories/XML.md)
