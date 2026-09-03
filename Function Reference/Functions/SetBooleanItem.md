# SetBooleanItem

## Description
Selects or deselects the specified check box or radio button.

```pascal
PROCEDURE SetBooleanItem(
				dialogID    : LONGINT;
				componentID : LONGINT;
				setState    : BOOLEAN);
```

```python
def vs.SetBooleanItem(dialogID, componentID, setState):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier for the radio or checkbox button component.|
|setState|BOOLEAN|The selection state to set for the given component.|

## Examples
```pascal
{* dialog init *}
SetupDialogC: BEGIN
	SetItemText(dialogID, 4, Num2StrF (0));
	SetItemText(dialogID, 6, Num2StrF (0));
	SetBooleanItem(dialogID, 7, FALSE);
	SelectEditText(dialogID, 4);
END;

BEGIN
	CASE item OF
		{* dialog init *}
		SetupDialogC: BEGIN
			SetBooleanItem(dialogID, 4, (method = 1));
			SetBooleanItem(dialogID, 5, (method = 2));

SetBooleanItem(gCurrentDialogID, 2*i + 5, gChangeField [fieldNum]);
```
```python
import vs

# Selects or deselects the specified check box or radio button.
dialogID = 1
componentID = 2
setState = True

vs.SetBooleanItem(dialogID, componentID, setState)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
