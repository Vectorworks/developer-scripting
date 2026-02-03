# PopupSetChoices

```pascal
PROCEDURE PopupSetChoices(
				recName     : DYNARRAY[] of CHAR;
				fieldName   : DYNARRAY[] of CHAR;
				popUpValues : ARRAY);
```

```python
def vs.PopupSetChoices(recName, fieldName, popUpValues):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|recName|DYNARRAY[] of CHAR|Name of record to which field will be added.|
|fieldName|DYNARRAY[] of CHAR|Name of field.|
|popUpValues|ARRAY|Enter popup values.|

## Examples
```pascal
PROCEDURE Example;

FUNCTION TestFunc(h :HANDLE) :BOOLEAN;
VAR
arrayText 		: ARRAY[1..3] OF STRING;
CurPopUpInfo 	: ARRAY[ 1..100 ] OF STRING;	
numPopUpValues 	: INTEGER;
i		: INTEGER;
BEGIN
	{create new record}
	NewField( 'Format-1', 'FieldNamePopUp', '22222', 17, 0 );

	arrayText[1] := '11111';
	arrayText[2] := '22222';
	arrayText[3] := '33333';
	
	{add new popup values to FieldNamePopUp}
	PopupSetChoices( 'Format-1', 'FieldNamePopUp', arrayText );

	{get popup values and print them}
	PopupGetChoices( 'Format-1', 'FieldNamePopUp', numPopUpValues, CurPopUpInfo );
	
	FOR i:=1 TO numPopUpValues DO
	BEGIN
		AlertInform ( CurPopUpInfo[ i ], '', FALSE );
	END;
	
	{clear popUp values}
	{NewField( 'Format-1', 'FieldNamePopUp', '22222', 17, 0 );}
END;

BEGIN
	ForEachObjectInLayer(TestFunc, 0, 0, 4);

END;
RUN(Example);
```

## Version
Availability: from Vectorworks 2023

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
