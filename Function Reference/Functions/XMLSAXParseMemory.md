# XMLSAXParseMemory

## Description
Parse an XML from memory using SAX.

```pascal
FUNCTION XMLSAXParseMemory(
				XMLHandle    : LONGINT;
				XMLData      : DYNARRAY[] of CHAR;
				nodeCallback : PROCEDURE): INTEGER;
```

```python
def vs.XMLSAXParseMemory(XMLHandle, XMLData, nodeCallback):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |
|XMLData|DYNARRAY[] of CHAR|   |
|nodeCallback|PROCEDURE|   |

## Examples
#### VectorScript ####
```pascal
PROCEDURE XMLSaxTest_Read;
CONST
	kExternalsFolder 		= 2;

	kSAXNODEType_StartDoc		= 1;
	kSAXNODEType_EndDoc		= 2;
	kSAXNODEType_StartNode		= 3;
	kSAXNODEType_EndNode		= 4;
	kSAXNODEType_Value		= 5;

VAR
	hXML    : LONGINT;
	result  : INTEGER;
	xmlFile : STRING;
	xmlData	: DYNARRAY [] OF CHAR;


  PROCEDURE XMLSAXNodeCallback(
  			     XMLHandle      :LONGINT;
  			     nodeType       :INTEGER;  {one of kSAXNODEType_ constants}
		             nodeName       :STRING;
		             nodeValue      :STRING;
		             nodeAttrs      :DYNARRAY [] OF CHAR);

  VAR
	I, foundAt : INTEGER;
	strType, attrName, attrValue : STRING;
	attrs, temp : DYNARRAY [] OF CHAR;
	foundAt1, foundAt2 : INTEGER;

  BEGIN
	CASE nodeType OF
		kSAXNODEType_StartDoc:	strType := 'StartDoc';
		kSAXNODEType_EndDoc:	strType := 'EndDoc';
		kSAXNODEType_StartNode:	strType := 'StartNode';
		kSAXNODEType_EndNode:	strType := 'EndNode';
		kSAXNODEType_Value:	strType := 'Value';
	END;

	AlrtDialog( Concat( 'type=', strType, Chr(13), 'node=', nodeName,  Chr(13), 'value=', nodeValue ) );

	IF Len(nodeAttrs) > 0 THEN BEGIN
		temp := nodeAttrs;
		attrs := '';
		{extract the attribute names and values for Ctr(13) delimited string}
		{<node name>Ctr(13)<nodeValue>Chr(13)}
		WHILE Len( temp ) > 0 DO BEGIN
			foundAt1 := Pos( Chr(13), temp );
			IF foundAt1 > 0 THEN BEGIN
				attrName := Copy( temp, 1, foundAt1 - 1 );
				{nodeAttrs := Copy( nodeAttrs, foundAt1 + 1, Len(nodeAttrs) - foundAt1 - 2 );}
				Delete( temp, 1, foundAt1 );
			END;

			foundAt2 := Pos( Chr(13), temp );
			IF foundAt2 > 0 THEN BEGIN
				attrValue := Copy( temp, 1, foundAt2 - 1 );
				{nodeAttrs := Copy( nodeAttrs, foundAt2 + 1, Len(nodeAttrs) - foundAt2 - 2 );}
				Delete( temp, 1, foundAt2 );
			END;

			IF (foundAt1 > 0) AND (foundAt2 > 0) THEN BEGIN
				attrs	:= Concat( attrs, ' ', attrName, '=', attrValue );
			END;
		END;

		AlrtDialog( Concat( 'node=', nodeName,  Chr(13), 'has attributes: ', attrs ) );
	END;
  END;


BEGIN
	hXML := InitXML;

	xmlData := '<myroot><data id="1" name="this is some name">value 1</data><data>value 2</data></myroot>';
	result := XMLSAXParseMemory( hXML, xmlData, XMLSAXNodeCallback );

	result := ReleaseXML(hXML);

END;
RUN(XMLSaxTest_Read);
```
#### Python ####
```python

```

## See Also
[InitXML](InitXML.md) | [ReleaseXML](ReleaseXML.md) | [XMLSAXParseFile](XMLSAXParseFile.md)

## Version
Availability: from Vectorworks 2011

## Category
* [XML SAX](../Categories/XML%20SAX.md)
