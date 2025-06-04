# GetThreeStateCheckBoxState

## Description
Retrieves the state of a Layout Manager three state checkbox.

```pascal
PROCEDURE GetThreeStateCheckBoxState(
				dialogID    : LONGINT;
				componentID : LONGINT;
				VAR iState  : INTEGER);
```

```python
def vs.GetThreeStateCheckBoxState(dialogID, componentID):
    return iState
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|iState|INTEGER|0-unchecked, 1-checked, 2-partially checked|

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
