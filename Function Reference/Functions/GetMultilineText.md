# GetMultilineText

## Description
Gets the text that is contained in the given componentID.

```pascal
PROCEDURE GetMultilineText(
				dialogID    : LONGINT;
				componentID : LONGINT;
				VAR text    : DYNARRAY[] of CHAR);
```

```python
def vs.GetMultilineText(dialogID, componentID):
    return text
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier of the component that the text will be retrieved from.|
|text|DYNARRAY[] of CHAR|The text of the component.|

## Examples
```pascal
17, 117, 217: BEGIN  {description text }
	CASE item OF
		17: BEGIN  { class description }
			gIsClassAttrsChanged [gClassIndex] := TRUE;
			GetMultilineText(dlogID, 17, description);
			gClassList [gClassIndex].Description := description;
		END;
```
```python
import vs

# Gets the text that is contained in the given componentID.
dialogID = 1
componentID = 2

result = vs.GetMultilineText(dialogID, componentID)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
