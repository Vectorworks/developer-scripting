# UpdateImagePushButton

## Description
Updates the image button created with CreateImagePushButton.

```pascal
PROCEDURE UpdateImagePushButton(
				dialogID       : LONGINT;
				controlID      : LONGINT;
				imageSpecifier : DYNARRAY[] of CHAR);
```

```python
def vs.UpdateImagePushButton(dialogID, controlID, imageSpecifier):
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
