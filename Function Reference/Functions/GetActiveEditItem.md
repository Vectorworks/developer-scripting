# GetActiveEditItem

## Description
Returns the active edit control in the specified dialog.  If no edit control has the focus, -1 is returned.

```pascal
FUNCTION GetActiveEditItem(dialogID : LONGINT): LONGINT;
```

```python
def vs.GetActiveEditItem(dialogID):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |

## Examples
```pascal
BEGIN
	activeItem := GetActiveEditItem(dlogID);
	IF (activeItem <> kProjectElevEdit) AND NOT (isProjectElevValid) THEN BEGIN
		isProjectElevValid := TRUE;
		ValidateProjElev;
		SetProjElevEditText;
```
```python
import vs

# Returns the active edit control in the specified dialog.
dialogID = 1

resultN = vs.GetActiveEditItem(dialogID)
vs.Message('GetActiveEditItem returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks12.0.1

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
