# CreateImagePushButton

## Description
Creates an image push button. Replaces CreateIconPushButton

```pascal
PROCEDURE CreateImagePushButton(
				dialogID          : LONGINT;
				controlID         : LONGINT;
				widthInCharacters : INTEGER;
				imageSpecifier    : DYNARRAY[] of CHAR);
```

```python
def vs.CreateImagePushButton(dialogID, controlID, widthInCharacters, imageSpecifier):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by the command to create the dialog.|
|controlID|LONGINT|The identifier that should be assigned to the control.|
|widthInCharacters|INTEGER|The width of the control.|
|imageSpecifier|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|

## Examples
```pascal
CreateImagePushButton( dialogID, VPLeftButton_ID, 8, 'IP Resources/Images/Camera Match/Vanish Left.png' );
SetFirstGroupItem( dialogID, VanishPtGroup_ID, VPLeftButton_ID );
```
```python
import vs

# Creates an image push button.
dialogID = 1
controlID = 2
widthInCharacters = 3
imageSpecifier = 'Example'

vs.CreateImagePushButton(dialogID, controlID, widthInCharacters, imageSpecifier)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
