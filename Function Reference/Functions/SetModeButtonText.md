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

## See Also
VS Functions:
[BeginModeButtonsText](BeginModeButtonsText.md) 
| [EndModeButtonsText](EndModeButtonsText.md)

## Version
Availability: from Vectorworks 2013

## Category
* [User Interactive](../Categories/User%20Interactive.md)
