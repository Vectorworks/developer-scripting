# CreateListBoxN

## Description
Creates a new list box control in a dialog layout. With isMultipleSelect true, the list supports multiple selection.

```pascal
PROCEDURE CreateListBoxN(
				dialogID           : LONGINT;
				itemID             : LONGINT;
				widthInCharacters  : LONGINT;
				heightInCharacters : LONGINT;
				isMultipleSelect   : BOOLEAN);
```

```python
def vs.CreateListBoxN(dialogID, itemID, widthInCharacters, heightInCharacters, isMultipleSelect):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|widthInCharacters|LONGINT|The width of the control in characters.|
|heightInCharacters|LONGINT|The height of the control in characters.|
|isMultipleSelect|BOOLEAN|Does the list support multiple selection|

## Examples
alogLayoutPulldownMenu}}

## Version
Availability: from VectorWorks10.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
