# GetFirstChild

## Description
Gets the last child within the specified element path. Use [ GetPreviousElement](GetPreviousElement.md) to step through the rest of the elements at the same nesting level.

```pascal
FUNCTION GetFirstChild(
				XMLHandle   : LONGINT;
				elementPath : STRING;
				VAR value   : STRING):INTEGER;
```

```python
def vs.GetFirstChild(XMLHandle, elementPath):
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
	IF GetFirstChild(hXML, xmlSL2LW, SLFieldName) = 0 THEN
	BEGIN
		IF GetObject(kSLFieldMapRec) <> NIL THEN DelObject(GetObject(kSLFieldMapRec));
		IF GetObject(kLWFieldMapRec) <> NIL THEN DelObject(GetObject(kLWFieldMapRec));
		 result := GetElementValue(hXML,Concat(xmlSL2LW,'/',SLFieldName), LWFieldName);
		 TempSLFieldName := Substitute(' ','_',SLFieldName);
			 IF result = 0 THEN
```
```python
import vs

# Gets the last child within the specified element path.
XMLHandle = 1
elementPath = 'C:/Temp'

resultN, value = vs.GetFirstChild(XMLHandle, elementPath)
vs.Message('GetFirstChild returned: ' + str((resultN, value)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
