# FindElement

## Description
Returns the element path of the specified element.

```pascal
FUNCTION FindElement(
				XMLHandle        : LONGINT;
				startElementPath : STRING;
				searchElement    : STRING;
				VAR foundPath    : STRING):INTEGER;
```

```python
def vs.FindElement(XMLHandle, startElementPath, searchElement):
    return (INTEGER, foundPath)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|startElementPath|STRING|   |
|searchElement|STRING|   |
|foundPath|STRING|Output parameter.|

## Examples
```pascal
 		xmlExpFlds := Concat('/',kSLDataFileTag,'/',kxmlExportFields);
UseDefaultFileErrorHandling(FALSE);
IF ReadXMLFile(hXML, -1, xmlFileNpath) <> 0 THEN
    result := CreateNewXMLDocument(hXML,kSLDataFileTag);
result := FindElement(hXML,Concat('/',kSLDataFileTag),kxmlExportFields,str);
IF result = 0 THEN
BEGIN
	{delete the existing export field list}
	result := DeleteElement(hXML,Concat(xmlExpFlds));

BEGIN {Get the status from the xml}
	result := GetElementValue(hXML, Concat(kSLPref,'/',kAutoUniverse), str);
	AutoU := Str2Boo(str);
END;
result := FindElement(hXML,kUDElement,Concat(kxmlSystem,System),str);
{This system exists in the xml file}
IF AutoU & (result =0) THEN
BEGIN
	RecHand := (GetObject(UniverseRecName));
```
```python
import vs

# Returns the element path of the specified element.
XMLHandle = 1
startElementPath = 'C:/Temp'
searchElement = 'Example'

resultN, foundPath = vs.FindElement(XMLHandle, startElementPath, searchElement)
vs.Message('FindElement returned: ' + str((resultN, foundPath)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
