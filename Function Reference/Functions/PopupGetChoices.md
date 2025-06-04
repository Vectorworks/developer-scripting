# PopupGetChoices

```pascal
PROCEDURE PopupGetChoices(
				recName            : DYNARRAY[] of CHAR;
				fieldName          : DYNARRAY[] of CHAR;
				VAR outNumValues   : INTEGER;
				VAR outPopUpValues : ARRAY);
```

```python
def vs.PopupGetChoices(recName, fieldName):
    return (outNumValues, outPopUpValues)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|recName|DYNARRAY[] of CHAR|Name of record in which field is.|
|fieldName|DYNARRAY[] of CHAR|Name of field.|
|outNumValues|INTEGER|Return number of popup values.|
|outPopUpValues|ARRAY|Return popup values.|

## Remarks
[[User:AHanson]], 2023.12.14:
This appears to work on standard resource records only and not with parametric object records when tested in v2024. Returns 0 and None. Use VS:GetLocalizedPluginChoice instead for Plug In Objects.

## Examples
```python
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
