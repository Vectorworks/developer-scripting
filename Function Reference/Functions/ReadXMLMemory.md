# ReadXMLMemory

## Description
Opens an XML file for reading from a string buffer.

```pascal
FUNCTION ReadXMLMemory(
				XMLHandle : LONGINT;
				XMLData   : DYNARRAY [] OF CHAR):INTEGER;
```

```python
def vs.ReadXMLMemory(XMLHandle, XMLData):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|XMLData|DYNARRAY [] OF CHAR|   |

## Examples
#### VectorScript ####
```pascal
procedure test;
var 	xml : longint;
	err : integer;
	mem : dynarray of char;
	value : string;

begin
	mem := '<root><value>34</value></root>';

	xml := InitXML;	

	err := ReadXMLMemory( xml, mem );
	err := GetElementValue( xml, '/root/value', value );


	AlrtDialog( Concat( 'value=', value ) );

	err := ReleaseXML( xml );
end;
run(test);
```
#### Python ####
```python

```

## See Also
[GetElementValue](GetElementValue.md) | [InitXML](InitXML.md) | [ReleaseXML](ReleaseXML.md) | [WriteXMLMemory](WriteXMLMemory.md)

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
