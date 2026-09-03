# GetPreviousElement

## Description
Gets the previous element in the same XML nesting level.

```pascal
FUNCTION GetPreviousElement(
				XMLHandle   : LONGINT;
				elementPath : STRING;
				VAR value   : STRING):INTEGER;
```

```python
def vs.GetPreviousElement(XMLHandle, elementPath):
    return (INTEGER, value)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|elementPath|STRING|   |
|value|STRING|Output parameter.|

## Examples
[XMLParse](examples/XMLParse.md)

```pascal
 BEGIN
 	NewField(kSLFieldMapRec,TempSLFieldName,LWFieldName,4,0);
NewField(kLWFieldMapRec,LWFieldName,TempSLFieldName,4,0);
 END;
     	WHILE GetPreviousElement(hXML, Concat(xmlSL2LW,'/',SLFieldName), SLFieldName) = 0 DO
     	BEGIN
     		result := GetElementValue(hXML, Concat(xmlSL2LW,'/',SLFieldName), LWFieldName);
     		TempSLFieldName := Substitute(' ','_',SLFieldName);
	IF result = 0 THEN
	BEGIN
		NewField(kSLFieldMapRec,TempSLFieldName,LWFieldName,4,0);
```
```python
import vs

# Gets the previous element in the same XML nesting level.
XMLHandle = 1
elementPath = 'C:/Temp'

resultN, value = vs.GetPreviousElement(XMLHandle, elementPath)
vs.Message('GetPreviousElement returned: ' + str((resultN, value)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
