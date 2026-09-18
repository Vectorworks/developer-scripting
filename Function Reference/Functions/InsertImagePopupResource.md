# InsertImagePopupResource

## Description
Inserts the indicated item of the specified resource list into the indicated image popup and returns the image popup index of the inserted item.
[MaKro] Inserts at end of image popup (appends). Index is 1-based and only for resource list.

```pascal
FUNCTION InsertImagePopupResource(
				dialogID    : LONGINT;
				componentID : LONGINT;
				listID      : LONGINT;
				index       : LONGINT): LONGINT;
```

```python
def vs.InsertImagePopupResource(dialogID, componentID, listID, index):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|index to the dialog layout that contains the image popup component.|
|componentID|LONGINT|index to a specific image popup component.|
|listID|LONGINT|an ID for a resource list created by the BuildResourceList function.|
|index|LONGINT|an index into the list.|

## Examples
#### VectorScript ####
```pascal
{ Add all items in the resource list to the image popup. }
for index:=1 to numItems do
index := InsertImagePopupResource(dialogID, kImagePopupID, listID,   index);
```
#### Python ####
```python
for idx in range(cnt_reslist):
    # append image to popup, 1-based index in resource list
    vs.InsertImagePopupResource(id_dlg, id_popup, id_reslist, idx + 1)
```

```pascal
BEGIN
IF symDefs[cnt].folderLevel = -2 THEN
	int := InsertImagePopupResource(selectSymbol, kSyms, defaultListID2, symDefs[cnt].resourceIndex)
ELSE
	int := InsertImagePopupResource(selectSymbol, kSyms, defaultListID, symDefs[cnt].resourceIndex);
END;

	EnableItem(dialog1, kOK, FALSE );
END
else BEGIN
	FOR cnt := 1 TO gNumShapes DO
		int := InsertImagePopupResource( dialog1, kImagePopup5, defConListID, cnt );

BEGIN
SymbolName := GetNameFromResourceList(ResourceListID,I);
idx := InsertImagePopupResource(SelectMarker, kImagePopup4,ResourceListID,I);
IF SymbolName = Marker1 THEN Marker1idx := idx;
idx := InsertImagePopupResource(SelectMarker, kImagePopup5,ResourceListID,I);
IF SymbolName = Marker2 THEN Marker2idx := idx;
END;
```
```python
import vs

# Inserts the indicated item of the specified resource list into the
# indicated image popup and returns the image popup index of the inserted
# item.
dialogID = 1
componentID = 2
listID = 3
index = 1

resultN = vs.InsertImagePopupResource(dialogID, componentID, listID, index)
vs.Message('InsertImagePopupResource returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
