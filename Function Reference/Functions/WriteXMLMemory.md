# WriteXMLMemory

## Description
Writes XML file into a dynamic string buffer.

```pascal
FUNCTION WriteXMLMemory(
				XMLHandle   : LONGINT;
				VAR XMLData : DYNARRAY [] OF CHAR):INTEGER;
```

```python
def vs.WriteXMLMemory(XMLHandle):
    return (INTEGER, XMLData)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|XMLData|DYNARRAY [] OF CHAR|Output parameter.|

## Examples
==== VectorScript ====
```pascal
procedure test;
var 	xml : longint;
	err : integer;
	mem : dynarray of char;
	value : string;

begin
	mem := '';

	xml := InitXML;	

	err := CreateNewXMLDocument( xml, 'root' );

	err := SetElementValue( xml, '/root/value', '34' );

	err := WriteXMLMemory( xml, mem );

	AlrtDialog( mem );

	err := ReleaseXML( xml );
end;
run(test);
```
==== Python ====
```python

```

## See Also
[CreateNewXMLDocument](CreateNewXMLDocument.md) | [SetElementValue](SetElementValue.md) | [InitXML](InitXML.md) | [ReleaseXML](ReleaseXML.md) | [ReadXMLMemory](ReadXMLMemory.md)

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
