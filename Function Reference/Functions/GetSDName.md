# GetSDName

## Description
Function GetSDName returns the name of the referenced symbol definition.

```pascal
FUNCTION GetSDName(h : HANDLE): STRING;
```

```python
def vs.GetSDName(h):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to symbol definition.|

## Examples
```pascal
16: BEGIN
		symDefCnt := symDefCnt + 1;
		CheckSymDefAlloc;
		symDefs[symDefCnt].folderName := folderDisplayName;
		symDefs[symDefCnt].symName := GetSDName(symHandle);
		symDefs[symDefCnt].folderLevel := folderLevel;
		symDefs[symDefCnt].resourceIndex := -1;
		IF symDefs[symDefCnt].symName = symName THEN selSymFolder := folderDisplayName;
	END;

resourceH := ImportResourceToCurrentFile( defConListID, cnt );
PIOHand := FInSymDef( resourceH );
gSymbolInfo [cnt].shapeName := GetName( GetRecord ( PIOHand, (NumRecords(PIOHand))) );
gSymbolInfo[cnt].deleteMe := TRUE;
gSymbolInfo[cnt].symbolName := GetSDName( resourceH );
gSymbolInfo[ cnt ].IsBadSymbol := IsSymbolBad( gSymbolInfo [cnt].shapeName, PIOHand );

FOR j := 1 TO numSymDefs DO BEGIN
	hSub := GetObject(SymDefNames[j]);
	IF (hSub <> NIL) THEN HSub2 := finsymdef(hSub);
	foreachobjectinlist(Scaleprim, 0, 2, HSub2);
	SetName(hSub, concat(getSDName(hSub), kDash, num2str(0, factor)));
END;
```
```python
import vs

# Function GetSDName returns the name of the referenced symbol definition.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

name = vs.GetSDName(h)
vs.Message('GetSDName returned: ' + str(name))
```
See also in tutorials: [28. Symbol Instance Schedule](ai%20examples/28_WorksheetSymbolSchedule.md)

## Version
Availability: from All Versions

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
