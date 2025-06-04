# SetCDATA

## Description
Sets the CDATA section of the specified element. The parameter elementPath is specified as a path of element names.

```pascal
FUNCTION SetCDATA(
				XMLHandle   : LONGINT;
				elementPath : STRING;
				data        : DYNARRAY [] OF CHAR):INTEGER;
```

```python
def vs.SetCDATA(XMLHandle, elementPath, data):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|elementPath|STRING|   |
|data|DYNARRAY [] OF CHAR|   |

## Examples
#### VectorScript ####
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
	err := SetCDATA( xml, '/root/data', 'custom data' );

	err := WriteXMLMemory( xml, mem );

	AlrtDialog( mem );

	err := ReleaseXML( xml );
end;
run(test);
```
#### Python ####
```python

```

## See Also
[GetCDATA](GetCDATA.md)

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
