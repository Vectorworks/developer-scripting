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

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
