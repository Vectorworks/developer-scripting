# AddButtonMode

## Description
Adds an image button to the mode bar for a tool. Replaces vstAddButtonMode.

```pascal
PROCEDURE AddButtonMode(imageSpecifier : DYNARRAY[] of CHAR);
```

```python
def vs.AddButtonMode(imageSpecifier):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|imageSpecifier|DYNARRAY[] of CHAR|The string identifier for the image. It should be of the form &quot;ResourceFileNameWithoutExtension/PathOfImageFile&quot;.|

## Examples
```pascal
{add a preferences button}
   AddButtonMode('Vectorworks/ModeViewBar/Options.svg');

	{add a preferences button}
{	vstAddButtonMode (kModeButton_7_ID); }
    AddButtonMode('Vectorworks/ModeViewBar/Options.svg');

{ ---------------------------------}
{ ------- OnToolDoSetup -----------}
{ ---------------------------------}
kOnToolDoSetupEventID: BEGIN
	AddButtonMode('VWMiscSmallImages/11016.png');
	BeginModeButtonsText;
	SetModeButtonText( GetPluginString( 6000 ), 2 );
	EndModeButtonsText;
	vstSetPtBehavior(kPolyPointTool);
```
```python
import vs

# Adds an image button to the mode bar for a tool.
imageSpecifier = 'Example'

vs.AddButtonMode(imageSpecifier)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
