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

## Examples
```pascal
{	CreateControl( dialogID, 65, 1, '', 28201 ); }
    CreateImageControl2(dialogID, 65, 0, 0, 'VWMiscImages/28201.png');

BEGIN
dialogID := CreateLayout (title, FALSE, OKString, CancelString);
IF icon > 0 THEN { CreateControl (dialogID, 4, 1, '', 17001); }
    CreateImageControl2(dialogID, 4, 0, 0, 'VWMiscImages/17001.png');
CreateStaticText (dialogID, 5, theMessage, width);

CreateImageControl2( dialogID, ShuttleIconLeft_ID, kSliderIconWidth, kSliderIconHeight, 'IP Resources/Images/Camera Match/Vanish Left Far.png' );
SetFirstGroupItem( dialogID, ShuttleSliderGroup_ID, ShuttleIconLeft_ID );
```
```python
import vs

dialogID = 1
controlID = 2
widthInPixels = 3
heightInPixels = 10
imageSpecifier = 'Example'

vs.CreateImageControl2(dialogID, controlID, widthInPixels, heightInPixels, imageSpecifier)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
