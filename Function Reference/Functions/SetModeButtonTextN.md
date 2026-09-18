# SetModeButtonTextN

## Description
Sets a mode bar button help text.

```pascal
PROCEDURE SetModeButtonTextN(
				modeName : STRING;
				modeHelp : STRING;
				modeType : INTEGER);
```

```python
def vs.SetModeButtonTextN(modeName, modeHelp, modeType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|modeName|STRING|The name of the mode.|
|modeHelp|STRING|Help message of the mode|
|modeType|INTEGER|The type of the mode.        Types:            RadioMode = 0,            ButtonMode = 1,            PrefButtonMode = 2,            CheckMode = 3,            EditTextMode = 4,            PullDownMode = 5|

## Examples
```pascal
BeginModeButtonsText;

SetModeButtonTextN( 'Mode1', 'help msg 1', 1 );

SetModeButtonTextN( 'Mode2', 'help msg 2', 0 );

EndModeButtonsText;
```

```pascal
{set the beginning baloon help string}
vstSetModeHelpBase (11045);
BeginModeButtonsText;
SetModeButtonTextN( GetPluginString( kOval ), 				GetPluginString( 7001 ), 0 );
SetModeButtonTextN( GetPluginString( kRectangular ), 		GetPluginString( 7002 ), 0 );
SetModeButtonTextN( GetPluginString( kRegularPolygon ), 	GetPluginString( 7003 ), 0 );
SetModeButtonTextN( GetPluginString( kFreehandPolygon ), 	GetPluginString( 7004 ), 0 );
SetModeButtonTextN( GetPluginString( kPreferences ), 		GetPluginString( 7005 ), 2 );

{set the beginning baloon help string}
vstSetModeHelpBase (kModeButton_1_ID);
BeginModeButtonsText;
SetModeButtonTextN( GetPluginString( 3001 ), GetPluginString( 8001 ), 0 );
SetModeButtonTextN( GetPluginString( 3002 ), GetPluginString( 8002 ), 0 );
SetModeButtonTextN( GetPluginString( 3003 ), GetPluginString( 8003 ), 0 );
SetModeButtonTextN( GetPluginString( 3004 ), GetPluginString( 8004 ), 0 );
SetModeButtonTextN( GetPluginString( 3005 ), GetPluginString( 8005 ), 0 );
```
```python
import vs

# Sets a mode bar button help text.
modeName = 'Example'
modeHelp = 'Example'
modeType = 0

vs.SetModeButtonTextN(modeName, modeHelp, modeType)
```

## See Also
VS Functions:
[BeginModeButtonsText](BeginModeButtonsText.md)| [EndModeButtonsText](EndModeButtonsText.md)

## Version
Availability: from Vectorworks 2026

## Category
* [User Interactive](../Categories/User%20Interactive.md)
