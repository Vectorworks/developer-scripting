# UpdateImageControl3

## Description
Updates the image control.<BR>
<BR>
Returns false if the image cannot be found or set to the control, otherwise returns true.<BR>
 <BR>
This function directly looks for the image file with the input file path, while UpdateImageControl2() only looks into the Vectorworks resrouces folder.

```pascal
FUNCTION UpdateImageControl3(
				dialogID      : LONGINT;
				controlID     : LONGINT;
				imageFullPath : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.UpdateImageControl3(dialogID, controlID, imageFullPath):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by the command to create the dialog.|
|controlID|LONGINT|The identifier of the control to be updated.|
|imageFullPath|DYNARRAY[] of CHAR|The full path to the image.|

## See Also
VS Functions:
[UpdateImageControl2](UpdateImageControl2.md)

## Version
Availability: from Vectorworks 2018

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
