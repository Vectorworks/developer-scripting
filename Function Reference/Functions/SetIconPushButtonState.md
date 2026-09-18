# SetIconPushButtonState

## Description
Retrieves the state of the specified Layout Manager icon push button (pressed or not pressed).

```pascal
FUNCTION SetIconPushButtonState(
				nDialogID    : LONGINT;
				nComponentID : LONGINT;
				bPressed     : BOOLEAN): BOOLEAN;
```

```python
def vs.SetIconPushButtonState(nDialogID, nComponentID, bPressed):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|bPressed|BOOLEAN|   |

## Examples
```pascal
BEGIN
	LiveSliderReleaseProc;
	boo := SetIconPushButtonState( dialogID, VPLeftButton_ID,	FALSE );
	boo := SetIconPushButtonState( dialogID, VPRightButton_ID,	FALSE );
	boo := SetIconPushButtonState( dialogID, VPUpButton_ID,		FALSE );
	boo := SetIconPushButtonState( dialogID, FOVButton_ID,		FALSE );
	boo := SetIconPushButtonState( dialogID, TiltButton_ID,	FALSE );
```
```python
import vs

# Retrieves the state of the specified Layout Manager icon push button
# (pressed or not pressed).
nDialogID = 1
nComponentID = 2
bPressed = True

ok = vs.SetIconPushButtonState(nDialogID, nComponentID, bPressed)
if ok:
    vs.Message('SetIconPushButtonState succeeded')
else:
    vs.Message('SetIconPushButtonState failed')
```

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
