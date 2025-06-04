# GetCDATA

## Description
Retrieves the CDATA section of the specified element. The parameter elementPath is specified as a path of element names.

```pascal
FUNCTION GetCDATA(
				XMLHandle     : LONGINT;
				elementPath   : STRING;
				VAR returnVal : DYNARRAY [] OF CHAR):INTEGER;
```

```python
def vs.GetCDATA(XMLHandle, elementPath):
    return (INTEGER, returnVal)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|elementPath|STRING|   |
|returnVal|DYNARRAY [] OF CHAR|Output parameter.|

## Examples
==== VectorScript ====
```pascal
procedure test;
var 	xml : longint;
	err : integer;
	mem : dynarray of char;
	value : string;
	cdata : dynarray of char;

begin
	mem := '<root><value>34</value><data><![CDATA[custom data]]></data></root>';

	xml := InitXML;	

	err := ReadXMLMemory( xml, mem );
	err := GetElementValue( xml, '/root/value', value );
	err := GetCDATA( xml, '/root/data', cdata );


	AlrtDialog( Concat( 'value=', value, ' cdata=', cdata ) );

	err := ReleaseXML( xml );
end;
run(test);
```
==== Python ====
```python
def test():
	mem = '<root><value>34</value><data><![CDATA[custom data]]></data></root>'
	xml = vs.InitXML()
	err = vs.ReadXMLMemory( xml, mem )
	err, value = vs.GetElementValue( xml, '/root/value' )
	err, cdata = vs.GetCDATA( xml, '/root/data',  )

	vs.AlrtDialog( vs.Concat( 'value=', value, ' cdata=', cdata ) )
	err = vs.ReleaseXML( xml )

test()
```

## See Also
[SetCDATA](SetCDATA.md)

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
