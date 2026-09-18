# FInSymDef

## Description
Function FInSymDef returns a handle to the first component object within the referenced symbol definition.

```pascal
FUNCTION FInSymDef(sdHd : HANDLE): HANDLE;
```

```python
def vs.FInSymDef(sdHd):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sdHd|HANDLE|Handle to symbol definition.|

## Examples
```pascal
BEGIN
CASE GetType(GetParent(parmHand)) OF
	11: ForEachObjectInList(Reset_Selection, 2, 0, FInGroup(GetParent(parmHand)));
	16: ForEachObjectInList(Reset_Selection, 2, 0, FInSymDef(GetParent(parmHand)));
	END;

BEGIN
	numSymbols := numSymbols + 1;
	traverseGroups (FinSymDef (symDefH));
	ResetObject (symDefH);
END;

sourceObjectHandle := FInSymDef( styleHandle );
IF ( (sourceObjectHandle <> NIL) & (GetTypeN( sourceObjectHandle ) = 86)  ) THEN
BEGIN
	architHeightStyleType := GetParamStyleType( gPluginH, kArchitHeightParam );
	structHeightStyleType := GetParamStyleType( gPluginH, kStructHeightParam );
```
```python
hSymDef = vs.FInSymDef( vs.GetObject( strMarkerActualName ) )
```

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
