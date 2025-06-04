# GetIconPushButtonState

## Description
Retrieves the state of the specified Layout Manager icon push button (pressed or not pressed).

```pascal
FUNCTION GetIconPushButtonState(
				nDialogID    : LONGINT;
				nComponentID : LONGINT;
				VAR bPressed : BOOLEAN): BOOLEAN;
```

```python
def vs.GetIconPushButtonState(nDialogID, nComponentID):
    return (BOOLEAN, bPressed)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|bPressed|BOOLEAN|   |

## Remarks
Julian [2013/03/07]
As of Vw 2013 SP2 (177995), this call works differently on Mac and Windows due<br />
to a bug. Here is an example of how it needs to be used on both platforms.<br />
The example toggles the state of the icon push button:

'''MAC''':<br />
Flag := GetIconPushButtonState(DialogID, item, Flag2);<br />
Flag := SetIconPushButtonState(DialogID, item, Flag2);

'''WIN''':<br />
Flag := GetIconPushButtonState(DialogID, item, Flag2);<br />
Flag := SetIconPushButtonState(DialogID, item, NOT Flag2);

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
