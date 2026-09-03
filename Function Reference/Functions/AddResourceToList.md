# AddResourceToList

## Description
Adds the indicated resource to the specified resource list, if it is of the same type as the items already in the list.  Returns the index of the resource in the list or 0.

```pascal
FUNCTION AddResourceToList(
				listID   : LONGINT;
				resource : HANDLE): LONGINT;
```

```python
def vs.AddResourceToList(listID, resource):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|listID|LONGINT|an ID for a resource list created by the BuildResourceList command.|
|resource|HANDLE|a resource to add to the resource list.|

## Examples
[AddHatchToResource](examples/AddHatchToResource.md)

```pascal
 		ELSE
 			SeatingSymHand := ImportResourceToCurrentFile(SymbolListID2,Index-NumSymbols);
 		IF SeatingSymHand <> NIL THEN SelectedSymbolName := GetName(SeatingSymHand);
  		IF CustDialog THEN
  			cnt := AddResourceToList(SymbolListID, GetObject(SelectedSymbolName));
  		RemoveAllImagePopupItems(dialog, kSeatSymbolPick);
  		NumSymbols := ResourceListSize(SymbolListID);
  		For cnt := 1 to NumSymbols DO
BEGIN

		IF GetActualNameFromResourceList(BreakOutLblListIDX,I) = symName THEN
			Found := TRUE;
	END;
	IF NOT Found THEN
		I := AddResourceToList(BreakOutLblListIDX,theSymDef);
END;

	For index := 1 to MultiHeadSymListCnt DO
		IF GetActualNameFromResourceList(MultiHeadSymListIdx,index) = symDefName THEN
			Found := TRUE;
	IF NOT Found THEN
		index := AddResourceToList(MultiHeadSymListIdx,theObj);
END;
```
```python
import vs

# Adds the indicated resource to the specified resource list, if it is of the
# same type as the items already in the list.
listID = 1
resource = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.AddResourceToList(listID, resource)
vs.Message('AddResourceToList returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
