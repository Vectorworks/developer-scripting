# GetElementValue

## Description
Returns the value of the element corresponding to the specified element name.  The parameter elementPath is specified as a path of element names. The return value is the error code (0 for no error, or non-0 if it failed). See [ InitXML](InitXML.md) for a list of the error codes.

The elementPath variable can be the explicit path, or you can use index notation to reference elements which all have the same xml tag:
 result := GetElementValue(hXML, '/geo/cloud/vector[2]/', str1);

```pascal
FUNCTION GetElementValue(
				XMLHandle   : LONGINT;
				elementPath : STRING;
				VAR value   : STRING):INTEGER;
```

```python
def vs.GetElementValue(XMLHandle, elementPath):
    return (INTEGER, value)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|elementPath|STRING|   |
|value|STRING|Output parameter.|

## Examples
```pascal
BEGIN
	IF GetElementValue(xmlID, Concat('/Preferences/', element), value) = 0
		THEN GetElement := value
		ELSE GetElement := '';
END;

BEGIN
	IF GetObject(kSLFieldMapRec) <> NIL THEN DelObject(GetObject(kSLFieldMapRec));
	IF GetObject(kLWFieldMapRec) <> NIL THEN DelObject(GetObject(kLWFieldMapRec));
	 result := GetElementValue(hXML,Concat(xmlSL2LW,'/',SLFieldName), LWFieldName);
	 TempSLFieldName := Substitute(' ','_',SLFieldName);
		 IF result = 0 THEN
		 BEGIN
		 	NewField(kSLFieldMapRec,TempSLFieldName,LWFieldName,4,0);

BEGIN {Get the status from the xml}
	result := GetElementValue(hXML, Concat(kSLPref,'/',kAutoUniverse), str);
	AutoU := Str2Boo(str);
END;
```
```python
import vs

# Returns the value of the element corresponding to the specified element name.
XMLHandle = 1
elementPath = 'C:/Temp'

resultN, value = vs.GetElementValue(XMLHandle, elementPath)
vs.Message('GetElementValue returned: ' + str((resultN, value)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
