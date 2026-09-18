# AddRadioMode

## Description
Adds a group of buttons with an image to the mode bar for a tool. Replaces vstAddRadioMode

```pascal
PROCEDURE AddRadioMode(
				initialSetting  : INTEGER;
				buttonCount     : INTEGER;
				imageSpecifier1 : DYNARRAY[] of CHAR;
				imageSpecifier2 : DYNARRAY[] of CHAR;
				imageSpecifier3 : DYNARRAY[] of CHAR;
				imageSpecifier4 : DYNARRAY[] of CHAR;
				imageSpecifier5 : DYNARRAY[] of CHAR;
				imageSpecifier  : DYNARRAY[] of CHAR);
```

```python
def vs.AddRadioMode(initialSetting, buttonCount, imageSpecifier1, imageSpecifier2, imageSpecifier3, imageSpecifier4, imageSpecifier5, imageSpecifier):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|initialSetting|INTEGER|   |
|buttonCount|INTEGER|   |
|imageSpecifier1|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|
|imageSpecifier2|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|
|imageSpecifier3|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|
|imageSpecifier4|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|
|imageSpecifier5|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|
|imageSpecifier|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|

## Examples
```pascal
{add the first mode group with three buttons}
   AddRadioMode(modeValue_1, 4, 'Vectorworks/ModeViewBar/Oval_Mode.svg', 'Vectorworks/ModeViewBar/Rectangle_Mode.svg', 'Vectorworks/ModeViewBar/Vertex_Mode.svg', 'Vectorworks/ModeViewBar/Freehand_Mode.svg', '', '');

	{add the first mode group with four buttons}
{	vstAddRadioMode (modeValue_1, 4, kModeButton_1_ID, kModeButton_2_ID, kModeButton_3_ID, kModeButton_4_ID, 0, 0); }
    AddRadioMode(modeValue_1, 4, 'Vectorworks/ModeViewBar/Oval_Mode.svg', 'Vectorworks/ModeViewBar/Rectangle_Mode.svg', 'Vectorworks/ModeViewBar/Vertex_Mode.svg', 'Vectorworks/ModeViewBar/Freehand_Mode.svg', '', '');

AddRadioMode( modeValue, 2, 'VWMiscSmallImages/11077.png', 'VWMiscSmallImages/11078.png', '', '', '', '' );
```
```python
import vs

# Adds a group of buttons with an image to the mode bar for a tool.
initialSetting = 1
buttonCount = 5
imageSpecifier1 = 'Example'
imageSpecifier2 = 'Example'
imageSpecifier3 = 'Example'
imageSpecifier4 = 'Example'
imageSpecifier5 = 'Example'
imageSpecifier = 'Example'

vs.AddRadioMode(initialSetting, buttonCount, imageSpecifier1, imageSpecifier2, imageSpecifier3, imageSpecifier4, imageSpecifier5, imageSpecifier)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
