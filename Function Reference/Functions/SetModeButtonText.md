# SetModeButtonText

## Description
Sets a mode bar button help text.

```pascal
PROCEDURE SetModeButtonText(
				modeName : STRING;
				modeType : INTEGER);
```

```python
def vs.SetModeButtonText(modeName, modeType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|modeName|STRING|The name of the mode.|
|modeType|INTEGER|The type of the mode.||Types:|RadioMode = 0,|ButtonMode = 1,|PrefButtonMode = 2,|CheckMode = 3,|EditTextMode = 4,|PullDownMode = 5|

## Examples
```pascal
BeginModeButtonsText;
SetModeButtonText( 'Mode1', 1 );
SetModeButtonText( 'Mode2', 0 );
EndModeButtonsText;
```

```pascal
BeginModeButtonsText;
SetModeButtonText( GetPluginString( kConstrLine ), 0 );
SetModeButtonText( GetPluginString( kUnconstrLine ), 0 );
EndModeButtonsText;

{ ---------------------------------}
kOnToolDoSetupEventID: BEGIN
	AddButtonMode('VWMiscSmallImages/11016.png');
	BeginModeButtonsText;
	SetModeButtonText( GetPluginString( 6000 ), 2 );
	EndModeButtonsText;
	vstSetPtBehavior(kPolyPointTool);
	vstSetModeHelpBase( -2322 );
END;

BeginModeButtonsText;
SetModeButtonText( GetPluginString( 3001 ), 0 );
SetModeButtonText( GetPluginString( 3002 ), 0 );
SetModeButtonText( GetPluginString( 3003 ), 0 );
SetModeButtonText( GetPluginString( 3004 ), 0 );
SetModeButtonText( GetPluginString( 3005 ), 0 );
```
```python
import vs

# Sets a mode bar button help text.
modeName = 'Example'
modeType = 0

vs.SetModeButtonText(modeName, modeType)
```

## See Also
VS Functions:
[BeginModeButtonsText](BeginModeButtonsText.md) 
| [EndModeButtonsText](EndModeButtonsText.md)

## Version
Availability: from Vectorworks 2013

## Category
* [User Interactive](../Categories/User%20Interactive.md)
