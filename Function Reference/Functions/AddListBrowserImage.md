# AddListBrowserImage

## Description
Adds an image to a list browser. Replaces AddLBImage.

```pascal
FUNCTION AddListBrowserImage(
				dialogID       : LONGINT;
				controlID      : LONGINT;
				imageSpecifier : DYNARRAY[] of CHAR): INTEGER;
```

```python
def vs.AddListBrowserImage(dialogID, controlID, imageSpecifier):
    return INTEGER
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
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
