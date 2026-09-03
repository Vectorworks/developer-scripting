# ReadXMLFile

## Description
Reads an XML file.  The entire file is read in, and parsed.  Once this has been done, the calling application can then use the following accessor functions to retrieve and modify the data within that file.  whichPath is the directory specifier; if whichPath is -1, the filename is taken by itself, without prepending a directory onto it.

```pascal
FUNCTION ReadXMLFile(
				XMLHandle : LONGINT;
				whichPath : INTEGER;
				filename  : STRING):INTEGER;
```

```python
def vs.ReadXMLFile(XMLHandle, whichPath, filename):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|whichPath|INTEGER|   |
|filename|STRING|   |

## Remarks
*\_c\_* (2016.06.16): Requires a HSF path (with colon) on Mac.

## Examples
[XMLParse](examples/XMLParse.md)

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
UseDefaultFileErrorHandling(FALSE);
IF ReadXMLFile(hXML, -1, xmlFileNpath) = 0 THEN
BEGIN
	ReadUniverseXML := TRUE;
	IF Len(System) <> 1 THEN System := '1';
	UniverseRecName := Concat(kNNAUniverseRec,System);
	gSystemElement := Concat(kUDElement,System);
	AutoU := FALSE;
```
```python
import vs

# Reads an XML file.
XMLHandle = 1
whichPath = 'C:/Temp'
filename = 'C:/Temp/example.txt'

resultN = vs.ReadXMLFile(XMLHandle, whichPath, filename)
vs.Message('ReadXMLFile returned: ' + str(resultN))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
