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

## See Also
VS Functions:
[BeginModeButtonsText](BeginModeButtonsText.md)| [EndModeButtonsText](EndModeButtonsText.md)

## Version
Availability: from Vectorworks 2026

## Category
* [User Interactive](Categories/User%20Interactive.md)

