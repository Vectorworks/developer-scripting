# SetThreeStateCheckBoxState

## Description
Sets the state of a Layout Manager three state checkbox.

```pascal
PROCEDURE SetThreeStateCheckBoxState(
				dialogID    : LONGINT;
				componentID : LONGINT;
				iState      : INTEGER);
```

```python
def vs.SetThreeStateCheckBoxState(dialogID, componentID, iState):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|iState|INTEGER|0-unchecked, 1-checked, 2-partially checked|

## Examples
```pascal
SetThreeStateCheckBoxState(1, 2, 3);
```
```python
import vs

# Sets the state of a Layout Manager three state checkbox.
dialogID = 1
componentID = 2
iState = 3

vs.SetThreeStateCheckBoxState(dialogID, componentID, iState)
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
