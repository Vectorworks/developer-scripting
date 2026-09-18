# SetElementValue

## Description
Sets the value of the specified element. The parameter elementPath is specified as a path of element names.

To reference multiple elements with the same elementPath, use bracket notation, as in the example.

```pascal
FUNCTION SetElementValue(
				XMLHandle   : LONGINT;
				elementPath : STRING;
				value       : STRING):INTEGER;
```

```python
def vs.SetElementValue(XMLHandle, elementPath, value):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|elementPath|STRING|   |
|value|STRING|   |

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
CONST
   xmlFileName  = 'C:XML Test File.xml';
VAR
   i :INTEGER;
   hXML :LONGINT;
   result :INTEGER;
BEGIN
   hXML := InitXML;
   result := CreateNewXMLDocument(hXML, 'XmlRoot');
   FOR i := 1 TO 3 DO BEGIN
      result := SetElementValue(hXML, Concat('/XmlRoot/list/loc[', i, ']'), Concat('i=',i));
      result := SetElementValue(hXML, Concat('/XmlRoot/list/pos[', i, ']'), Concat('i=',i));
   END;
   result := WriteXMLFile(hXML, -1, xmlFileName);
   Message('result: ', result);
   result := ReleaseXML(hXML);
END;
RUN(Example);
```
#### Python ####
```python

```

```pascal
BEGIN
	int := SetElementValue(xmlID, Concat('/Preferences/', element), value);
END;

	BEGIN
	TempNumFields := NumFields(RecHand);
result := SetElementValue(hXML, Concat(xmlExpFlds,'/',kAppStamp), kXMLVW);
result := SetElementValue(hXML, Concat(xmlExpFlds,'/',kTimeStamp), GetCurrentTime);
FOR I := 1 TO TempNumFields DO
	BEGIN
	SLField := GetFldName(RecHand,I);

result := SetElementValue  (TargetIndex, Concat('/',xmlRootName,'/',xmlSpeakerFolder,'/',Concat('BoxTotal')), Concat(BoxTTL));
```
```python
result = vs.SetElementValue(h, 'file.txt', value)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
