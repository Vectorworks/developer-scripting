# XMLSAXBeginDocMemory

## Description
Write XML using SAX, begin of a document in memory. [[VS:XMLSAXEndDocMemory| XMLSAXEndDocMemory]] ends a document.

```pascal
FUNCTION XMLSAXBeginDocMemory(XMLHandle : LONGINT): INTEGER;
```

```python
def vs.XMLSAXBeginDocMemory(XMLHandle):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |

## Examples
==== VectorScript ====
```pascal
PROCEDURE XMLSaxTest_Write;
CONST
	kExternalsFolder 		= 2;
VAR
	hXML    : LONGINT;
	result  : INTEGER;
	xmlFile : STRING;
	xmlData	: DYNARRAY [] OF CHAR;

BEGIN
	hXML := InitXML;

	result := XMLSAXBeginDocMemory( hXML);

	result := XMLSAXBeginNode( hXML, 'theRoot' );
		result := XMLSAXBeginNode( hXML, 'data' );
			result := XMLSAXAddNodeAttr( hXML, 'id', '1' );
			result := XMLSAXAddNodeAttr( hXML, 'name', 'none' );
			result := XMLSAXAddNodeValue( hXML, 'value1' );
		result := XMLSAXEndNode( hXML );

		result := XMLSAXBeginNode( hXML, 'data' );
			result := XMLSAXAddNodeValue( hXML, 'value2' );
		result := XMLSAXEndNode( hXML );

	result := XMLSAXEndNode( hXML );

	result := XMLSAXEndDoc( hXML );

	{ Writing to string XML }
	ALLOCATE xmlData[0 .. 255];
	result := XMLSAXEndDocMemory( hXML, xmlData );
	AlrtDialog( xmlData );

	result := ReleaseXML(hXML);

	AlrtDialog( Concat( 'done! result=', result ) );
END;
RUN(XMLSaxTest_Write);
```
==== Python ====
```python

```

## See Also
[InitXML](InitXML.md) | [ReleaseXML](ReleaseXML.md)

[XMLSAXEndDocMemory](XMLSAXEndDocMemory.md) | [XMLSAXBeginNode](XMLSAXBeginNode.md) | [XMLSAXEndNode](XMLSAXEndNode.md) | [XMLSAXAddNodeAttr](XMLSAXAddNodeAttr.md) | [XMLSAXAddNodeValue](XMLSAXAddNodeValue.md)

## Version
Availability: from Vectorworks 2011

## Category
* [XML SAX](../Categories/XML%20SAX.md)
