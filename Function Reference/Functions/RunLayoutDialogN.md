# RunLayoutDialogN

## Description
Displays the specified dialog and initiates the dialog event loop. The dialog event loop is specified in a procedure subroutine that is passed as a parameter to the function.

```pascal
FUNCTION RunLayoutDialogN(
				dialogID             : LONGINT;
				callback             : PROCEDURE;
				enableContextualHelp : BOOLEAN): LONGINT;
```

```python
def vs.RunLayoutDialogN(dialogID, callback, enableContextualHelp):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog to be displayed.|
|callback|PROCEDURE|The event loop subroutine for the dialog.|
|enableContextualHelp|BOOLEAN|Determines whether or not contextual help is accessible|

## Version
Availability: from Vectorworks 2018

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
