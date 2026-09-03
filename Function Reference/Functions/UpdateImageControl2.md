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

## Examples
```pascal
{	SetControlData( dialogID, 65, 28200+caseNum ); }
	TempI := 28200+caseNum;
    tmpStr2 := Concat('VWMiscImages/', TempI, '.png');
    UpdateImageControl2(dialogID, 65, tmpStr2);

	1: SetControlData (dlogID, 4, 17003);
	2: SetControlData (dlogID, 4, 17004);
	3: SetControlData (dlogID, 4, 17006);
}
	1: UpdateImageControl2 (dlogID, 4, 'VWMiscImages/17001.png');	{Exclamation Point}
	2: UpdateImageControl2 (dlogID, 4, 'VWMiscImages/17002.png');	{Question Mark}
	3: UpdateImageControl2 (dlogID, 4, 'VWMiscImages/17001.png');	{X}

BEGIN
	UpdateImageControl2( dialogID, ShuttleIconLeft_ID, 'IP Resources/Images/Camera Match/Vanish Left Far.png' );
	UpdateImageControl2( dialogID, ShuttleIconRight_ID, 'IP Resources/Images/Camera Match/Vanish Left Near.png' );
	SetItemText( dialogID, SliderModeStaTex, '' );
	PressModeButtonProc( item );
	SliderSetToAdjust := kAdjLeftVanishPt;
```
```python
import vs

# Updates the image control created with CreateImageControl2.
dialogID = 1
controlID = 2
imageSpecifier = 'Example'

vs.UpdateImageControl2(dialogID, controlID, imageSpecifier)
```

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
