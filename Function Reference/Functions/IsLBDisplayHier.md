# IsLBDisplayHier

## Description
Returns whether the indicated list browser is set to display items hierarchically. One column in the list browser can be set to display names hierarchically.

```pascal
FUNCTION IsLBDisplayHier(
				dialogID    : LONGINT;
				componentID : LONGINT): BOOLEAN;
```

```python
def vs.IsLBDisplayHier(dialogID, componentID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The id of the dialog containing the list browser.|
|componentID|LONGINT|The id of the list browser.|

## See Also
VS Functions:
[EnableLBHierDisplay](EnableLBHierDisplay.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
