# RunNamedDialog

## Description
Displays the specified dialog with universal name and initiates the dialog event loop. The dialog event loop is specified in a procedure subroutine that is passed as a parameter to the function.

```pascal
FUNCTION RunNamedDialog(
				dialogID : LONGINT;
				callback : PROCEDURE;
				univName : STRING): LONGINT;
```

```python
def vs.RunNamedDialog(dialogID, callback, univName):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog to be displayed|
|callback|PROCEDURE|The event loop subroutine for the dialog|
|univName|STRING|The universal name of the dialog|

## Remarks
[DWD 1/29/13]

## Examples
```pascal
dialogID := define_MainDialog;
dialogOK := VerifyLayout (dialogID);
exitState := RunNamedDialog (dialogID, getInfo_Main, 'ArcBySegLength');

BEGIN
	dialogID := defineDialog_Main;
	dialogOK := VerifyLayout (dialogID);
	exitState := RunNamedDialog (dialogID, displayDialog, 'ArcIntoSegments');

exitState := RunNamedDialog (dialogID, displayDialog, 'AttachRecord');
```
```python
import vs

# Displays the specified dialog with universal name and initiates the dialog
# event loop.
def handle_object(objHandle):
    vs.Message('Processing: ' + str(objHandle))

dialogID = 1
callback = handle_object
univName = 'Example'

resultN = vs.RunNamedDialog(dialogID, callback, univName)
vs.Message('RunNamedDialog returned: ' + str(resultN))
```

## See Also
VS Functions:
[RunLayoutDialog](RunLayoutDialog.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
