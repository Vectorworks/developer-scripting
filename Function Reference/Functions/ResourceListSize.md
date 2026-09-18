# ResourceListSize

## Description
Returns the number of items in the specified resource list.

```pascal
FUNCTION ResourceListSize(listID : LONGINT): LONGINT;
```

```python
def vs.ResourceListSize(listID):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|listID|LONGINT|an ID for a resouce list created by the BuildResourceList function.|

## Examples
#### VectorScript ####
```pascal
{ Update numItems as the number of items in the resource list has }
{ changed. }
numItems := ResourceListSize(listID);
```
#### Python ####
```python

```

```pascal
BEGIN
	FOR i := 1 TO ResourceListSize(listID) DO AddChoice(dialogID,  itemID,  GetNameFromResourceList(listID, i),  i-1);
END;

 		IF SeatingSymHand <> NIL THEN SelectedSymbolName := GetName(SeatingSymHand);
  		IF CustDialog THEN
  			cnt := AddResourceToList(SymbolListID, GetObject(SelectedSymbolName));
  		RemoveAllImagePopupItems(dialog, kSeatSymbolPick);
  		NumSymbols := ResourceListSize(SymbolListID);
  		For cnt := 1 to NumSymbols DO
BEGIN
Index := InsertImagePopupResource(dialog, kSeatSymbolPick,SymbolListID,cnt);
END;

CollectMultHeadSymNames;
{fieldStr := GetRField(PIOHan,PIOName,'HeadSym');}
booResult := vsoPrmName2WidgetID('','HeadSym', OutWidgID);
vsoWidgetPopupClear(OutWidgID);
MultiHeadSymListCnt := ResourceListSize(MultiHeadSymListIdx);
For index := 1 to MultiHeadSymListCnt DO
	BEGIN
	vsoWidgetPopupAdd(OutWidgID,GetActualNameFromResourceList(MultiHeadSymListIdx,index),GetActualNameFromResourceList(MultiHeadSymListIdx,index));
	END;
```
```python
result = vs.ResourceListSize(True)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
