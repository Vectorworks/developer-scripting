# ImportResourceToCurrentFile

## Description
Imports the indicated resource from the specified list to the current file, if it is not already in the current file, and returns the handle to the resource.

```pascal
FUNCTION ImportResourceToCurrentFile(
				listID : LONGINT;
				index  : LONGINT): HANDLE;
```

```python
def vs.ImportResourceToCurrentFile(listID, index):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|listID|LONGINT|an ID for a resource list created by the [BuildResourceList](BuildResourceList.md) and [BuildResourceListN](BuildResourceListN.md) command.|
|index|LONGINT|an index into the list.|

## Examples
[WorkingWithResrouceList](examples/WorkingWithResrouceList.md)

```pascal
ELSE IF shouldUseExisting THEN BEGIN
	IF selSymFolder = GetPluginString(4012) THEN BEGIN { symbol is in a defaults document }
		choiceNum := GetImagePopupSelectedItem(selectSymbol, kSyms);
		IF choiceNum <= defaultListCount THEN
			symHandle := ImportResourceToCurrentFile(defaultListID, choiceNum)
		ELSE
			symHandle := ImportResourceToCurrentFile(defaultListID2, choiceNum-defaultListCount);
		IF symHandle <> NIL THEN
			symName := GetName(symHandle);
		END

BEGIN
h := ImportResourceToCurrentFile(ResourceListID, I);
ImportedMarker1 := TRUE;
END

BEGIN
	resourceH := ImportResourceToCurrentFile( defConListID, cnt );
	PIOHand := FInSymDef( resourceH );
	gSymbolInfo [cnt].shapeName := GetName( GetRecord ( PIOHand, (NumRecords(PIOHand))) );
	gSymbolInfo[cnt].deleteMe := TRUE;
	gSymbolInfo[cnt].symbolName := GetSDName( resourceH );
```
```python
if vs.GetObject( strMarkerName ) == None:
	hResult = vs.ImportResourceToCurrentFile( hResourceListID, index )
	bMarkerImported = True
```

## See Also
VS Functions:
[ImportResToCurFileN](ImportResToCurFileN.md) | [BuildResourceList](BuildResourceList.md) |[BuildResourceListN](BuildResourceListN.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
