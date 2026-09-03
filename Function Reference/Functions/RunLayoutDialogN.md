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

## Examples
```pascal
resultN := RunLayoutDialogN(1, callback, TRUE);
```
```python
import vs

# Displays the specified dialog and initiates the dialog event loop.
def handle_object(objHandle):
    vs.Message('Processing: ' + str(objHandle))

dialogID = 1
callback = handle_object
enableContextualHelp = True

resultN = vs.RunLayoutDialogN(dialogID, callback, enableContextualHelp)
vs.Message('RunLayoutDialogN returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
