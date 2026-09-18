# SetHelpText

## Description
Sets the help text for the given component.

```pascal
PROCEDURE SetHelpText(
				dialogID    : LONGINT;
				componentID : LONGINT;
				helpText    : STRING);
```

```python
def vs.SetHelpText(dialogID, componentID, helpText):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|the dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier of the component for which to set the help text.|
|helpText|STRING|The help text to set for the given component.|

## Examples
```pascal
{* Set the help strings *}
SetHelpText(dialogID, 1, helpString [1]);
SetHelpText(dialogID, 2, helpString [2]);
SetHelpText(dialogID, 4, helpString [3]);
SetHelpText(dialogID, 6, helpString [4]);
SetHelpText(dialogID, 7, helpString [5]);

{* Set the help strings *}
	SetHelpText(dialogID, 1, GetPlugInString (3010));
	SetHelpText(dialogID, 2, GetPlugInString (3011));
	SetHelpText(dialogID, 4, GetPlugInString (3012));
	SetHelpText(dialogID, 5, GetPlugInString (3013));
	SetHelpText(dialogID, 6, GetPlugInString (3014));

{* Help Strings *}
	SetHelpText(dialogID, 1, GetPlugInString (3007));
	SetHelpText(dialogID, 2, GetPlugInString (3008));
	SetHelpText(dialogID, 6, GetPlugInString (3009));
	SetHelpText(dialogID, 8, GetPlugInString (3010));
```
```python
import vs

# Sets the help text for the given component.
dialogID = 1
componentID = 2
helpText = 'Example text'

vs.SetHelpText(dialogID, componentID, helpText)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
