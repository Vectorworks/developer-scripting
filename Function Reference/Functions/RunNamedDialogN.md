# RunNamedDialogN

## Description
Displays the specified dialog with universal name and initiates the dialog event loop. The dialog event loop is specified in a procedure subroutine that is passed as a parameter to the function.

```pascal
FUNCTION RunNamedDialogN(
				dialogID             : LONGINT;
				callback             : PROCEDURE;
				univName             : STRING;
				enableContextualHelp : BOOLEAN): LONGINT;
```

```python
def vs.RunNamedDialogN(dialogID, callback, univName, enableContextualHelp):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog to be displayed|
|callback|PROCEDURE|The event loop subroutine for the dialog|
|univName|STRING|The universal name of the dialog|
|enableContextualHelp|BOOLEAN|Determines whether or not contextual help is accessible|

## See Also
VS Functions:
[RunLayoutDialogN](RunLayoutDialogN.md)

## Version
Availability: from Vectorworks 2018

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
