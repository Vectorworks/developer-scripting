# GetBooleanItem

## Description
Determines if a radio or checkbox button is selected or not.

```pascal
PROCEDURE GetBooleanItem(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				VAR outState : BOOLEAN);
```

```python
def vs.GetBooleanItem(dialogID, componentID):
    return outState
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier for the radio or checkbox button component.|
|outState|BOOLEAN|True if the button is selected, false otherwise.|

## Examples
```pascal
1: BEGIN
	GetBooleanItem(dialogID, 7, gClick );

BEGIN
	fieldNum := gN1 [gDialogNum] + i - 1;
	GetBooleanItem(gCurrentDialogID, 2*i + 5, gChangeField [fieldNum]);

BEGIN
	GetBooleanItem(dialog1, kReconcileThese, reconcileThese );
	GetBooleanItem(dialog1, kVwText, vwText );
	EnableItem(dialog1, kLegacyTextNotes,   reconcileThese);
	EnableItem(dialog1, kLegacyKeyNotes,    reconcileThese);
	EnableItem(dialog1, kLegacyGenNotes,    reconcileThese);
```
```python
import vs

# Determines if a radio or checkbox button is selected or not.
dialogID = 1
componentID = 2

result = vs.GetBooleanItem(dialogID, componentID)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
