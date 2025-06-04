# GetPopUpChoiceIndex

## Description
Gets the zero based index of the first choice in the pop-up which has itemText name. If there is no choice named itemText in the pop-up itemIndex is set to -1.

```pascal
PROCEDURE GetPopUpChoiceIndex(
				dialogID      : LONGINT;
				componentID   : LONGINT;
				itemText      : STRING;
				VAR itemIndex : INTEGER);
```

```python
def vs.GetPopUpChoiceIndex(dialogID, componentID, itemText):
    return itemIndex
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier of the component which choice index will be retrieved from by a given choice name.|
|itemText|STRING|The name of the choice which index will be obtained.|
|itemIndex|INTEGER|The index of the given choice's string in the pop-up. If there are duplicate choice name itemIndex is the index of the first choice having itemText name.|

## Version
Availability: from Vectorworks 2011

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
