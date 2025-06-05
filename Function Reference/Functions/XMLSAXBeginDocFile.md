# XMLSAXBeginDocFile

## Description
Write XML using SAX, begin of a document file. [ MLSAXEndDoc](XMLSAXEndDoc.md) ends a document.

```pascal
FUNCTION XMLSAXBeginDocFile(
				XMLHandle : LONGINT;
				whichPath : INTEGER;
				filename  : STRING): INTEGER;
```

```python
def vs.XMLSAXBeginDocFile(XMLHandle, whichPath, filename):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|whichPath|INTEGER|   |
|filename|STRING|   |

## Examples
#### VectorScript ####
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

	xmlFile := 'XML Test File OUTPUT.xml';
	result := XMLSAXBeginDocFile( hXML, kExternalsFolder, xmlFile );

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

	result := ReleaseXML(hXML);

	AlrtDialog( Concat( 'done! result=', result ) );
END;
RUN(XMLSaxTest_Write);
```
#### Python ####
```python

```

## See Also
[InitXML](InitXML.md) | [ReleaseXML](ReleaseXML.md)

[XMLSAXEndDoc](XMLSAXEndDoc.md) | [XMLSAXBeginNode](XMLSAXBeginNode.md) | [XMLSAXEndNode](XMLSAXEndNode.md) | [XMLSAXAddNodeAttr](XMLSAXAddNodeAttr.md) | [XMLSAXAddNodeValue](XMLSAXAddNodeValue.md)

## Version
Availability: from Vectorworks 2011

## Category
* [XML SAX](../Categories/XML%20SAX.md)
