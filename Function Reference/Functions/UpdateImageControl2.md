# UpdateImageControl2

## Description
Updates the image control created with CreateImageControl2

```pascal
PROCEDURE UpdateImageControl2(
				dialogID       : LONGINT;
				controlID      : LONGINT;
				imageSpecifier : DYNARRAY[] of CHAR);
```

```python
def vs.UpdateImageControl2(dialogID, controlID, imageSpecifier):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by the command to create the dialog.|
|controlID|LONGINT|The identifier of the control to be updated.|
|imageSpecifier|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
