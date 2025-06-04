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

## See Also
VS Functions:
[RunLayoutDialog](RunLayoutDialog.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
