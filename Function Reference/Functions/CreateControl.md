# CreateControl

## Description
**[Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md) DEPRECATED after Vectorworks2012**. See [CreateImageControl2](CreateImageControl2.md) and [CreateThumbnailPopup](CreateThumbnailPopup.md) for a replacement.

Creates a new extended dialog control item. Supported extended dialog controls include image, system color palette, and slider controls.

```pascal
PROCEDURE CreateControl(
				dialogID    : LONGINT;
				itemID      : LONGINT;
				controlKind : LONGINT;
				name        : STRING;
				data        : LONGINT);
```

```python
def vs.CreateControl(dialogID, itemID, controlKind, name, data):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|controlKind|LONGINT|The type of control item.|
|name|STRING|The display text of the control item.|
|data|LONGINT|Initial data for the control item.|

## Remarks

**Table - Control Types**

| Index | Control Type    | Data |
|-------|----------------|------|
| 1     | PICT Image     | Resource ID of a PICT<br>Use [CreateImageControl2](CreateImageControl2.md) from VW 2012 |
| 2     | System Color   | Ignored. Pass a value of 0 |
| 3     | Slider         | Maximum value of slider whose range is 0 - ### |
| 10    | Image Popup    | Ignored. Pass a value of 0.<br>Use [CreateThumbnailPopup](CreateThumbnailPopup.md) from VW 2012 |
| 11    | Gradient Slider| Width of the slider in characters |
| 26    | PNG Image      | Resource ID of a PNG image<br>Use [CreateImageControl2](CreateImageControl2.md) from VW 2012 |

Check out the full example Align Selected Objects.
http://www.vectorworks.net/support/custom/vscript/example.php
It contains a working example on a modern dialogue with an image control.

## Examples
#### VectorScript ####
```pascal
{Slider Control Example}
PROCEDURE dialog1_Main;
CONST
kSlider = 4;
kLabel  = 5;
kValue  = 6;
VAR
dialog1   :INTEGER;
gSlider   :LONGINT;

PROCEDURE dialog1_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
CASE item OF
kSlider:
BEGIN
GetControlData(dialog1, kSlider, gSlider);
SetField(kValue, Concat(gSlider));
END;
END;
END;

BEGIN
gSlider := 1000;
dialog1 := CreateLayout('Slider Control', FALSE, 'OK', 'Cancel');
CreateControl     (dialog1, kSlider,  3, '', 1000);
CreateStaticText  (dialog1, kLabel,   'Slider Value:', -1);
CreateStaticText  (dialog1, kValue,   ' ', -1);
SetFirstLayoutItem(dialog1, kSlider);
SetBelowItem      (dialog1, kSlider,  kLabel,   0, 0);
SetRightItem      (dialog1, kLabel,   kValue,   0, 0);
IF RunLayoutDialog(dialog1, dialog1_Handler) = 1 THEN BEGIN
END;
END;
RUN(dialog1_Main);
```
#### Python ####
```python
#{Slider Control Example}
def dialog1_Handler(item , data):
	if item == kSlider:
		vs.GetControlData(dialog1, kSlider, gSlider);
	
def dialog1_Main():

	global kSlider
	global kLabel
	global kValue
	global dialog1
	global gSlider

	kSlider = 4
	kLabel  = 5
	kValue  = 6

	gSlider = 1000
	dialog1 = vs.CreateLayout('Slider Control', False, 'OK', 'Cancel')
	vs.CreateControl     (dialog1, kSlider,  3, '', 1000)
	vs.CreateStaticText  (dialog1, kLabel,   'Slider Value:', -1)
	vs.CreateStaticText  (dialog1, kValue,   ' ', -1)
	vs.SetFirstLayoutItem(dialog1, kSlider)
	vs.SetBelowItem      (dialog1, kSlider,  kLabel,   0, 0)
	vs.SetRightItem      (dialog1, kLabel,   kValue,   0, 0)

	if vs.RunLayoutDialog(dialog1, dialog1_Handler) == 1:
		pass

kSlider = 0
kLabel = 0
kValue = 0
dialog1 = 0
gSlider = 0
dialog1_Main()
```

```pascal
CreateCheckBox(dialogID,69,GetPlugInString(6069));
CreateCheckBox(dialogID,68,GetPlugInString(6068));
CreateStaticText(dialogID,70,'',40);
CreateEditText(dialogID,71,'',40);
CreateControl(dialogID, 72, 2, '', 0);
CreateControl(dialogID, 73, 2, '', 0);
CreateControl(dialogID, 74, 2, '', 0);
CreateControl(dialogID, 75, 2, '', 0);

CreateControl( dialogID, ShuttleSlider_ID, 3, 'Shuttle', 2 * kHalfShuttleSliderRange );
SetRightItem( dialogID, ShuttleIconLeft_ID, ShuttleSlider_ID, 0, 0 );

CreateGroupBox (dialogID, 3, GetPluginString (3008), TRUE);
CreateStaticText (dialogID, 4, GetPluginString (3009), -1);
CreateControl (dialogID, 5, 3, '', kMaxSpeed);
CreateStaticText (dialogID, 6, GetPluginString (3010), -1);
```
```python
import vs

# **Vectorworks 2012 Deprecated Functions DEPRECATED after Vectorworks2012**.
dialogID = 1
itemID = 2
controlKind = 0
name = 'Example'
data = 3

vs.CreateControl(dialogID, itemID, controlKind, name, data)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks 9.0, deprecated from VW 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
