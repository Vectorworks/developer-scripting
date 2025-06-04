# CreateImageControl2

```pascal
PROCEDURE CreateImageControl2(
				dialogID       : LONGINT;
				controlID      : LONGINT;
				widthInPixels  : INTEGER;
				heightInPixels : INTEGER;
				imageSpecifier : DYNARRAY[] of CHAR);
```

```python
def vs.CreateImageControl2(dialogID, controlID, widthInPixels, heightInPixels, imageSpecifier):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by the command to create the dialog.|
|controlID|LONGINT|The identifier that should be assigned to the control.|
|widthInPixels|INTEGER|The width of the control. Use zero to let the image dictate the dimension|
|heightInPixels|INTEGER|The height of the control. Use zero to let the image dictate the dimension|
|imageSpecifier|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
