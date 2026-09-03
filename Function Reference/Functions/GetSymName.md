# GetSymName

## Description
Function GetSymName returns the symbol name of a referenced symbol in a VectorWorks document.

```pascal
FUNCTION GetSymName(symHd : HANDLE): STRING;
```

```python
def vs.GetSymName(symHd):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|symHd|HANDLE|Handle to placed symbol.|

## Examples
```pascal
BEGIN
	PopSub1(dialogID, 9, type2DO);
	for i := 1 to handle_cnt do BEGIN
		if type1Va = types[15] then str := GetSymName(handles[i]) ELSE {*****}
		IF type1Va = types[86] THEN str := GetName(GetRecord(handles[i], NumRecords(handles[i]))); {*****}
		PopSub2;
	END;

	resourceH := GetObject( gImagePopup5Str );
	PIOHand := FInSymDef( resourceH );
	gSymbolInfo [cnt].shapeName := GetName( GetRecord (PIOHand, (NumRecords(PIOHand))));
	gSymbolInfo[cnt].deleteMe := FALSE;
	gSymbolInfo[cnt].symbolName := GetSymName( resourceH );
	gSymbolInfo[cnt].isBadSymbol := IsSymbolBad( gSymbolInfo [cnt].shapeName, PIOHand );
END;	{of GetResourceFromList( defConListID, cnt ) <> NIL}

BEGIN
tempstr := getsymname(h);
tempstr := copy(tempstr, 1, CharLocR(tempstr, kDash)-1);
IF kDebugMode THEN alrtdialog(concat('GETSHORTSYMNAME: output is ', tempstr));
GetShortSymName := tempstr;
END;
```
```python
import vs

# Function GetSymName returns the symbol name of a referenced symbol in a
# VectorWorks document.
symHd = vs.FSActLayer()  # handle to the first selected object on the active layer

name = vs.GetSymName(symHd)
vs.Message('GetSymName returned: ' + str(name))
```

## Version
Availability: from All Versions

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
