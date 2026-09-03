# RemoveEnhancedPullDownMenuItemRange

## Description
Removes the specified range of items from the specified Layout Manager enhanced pull down menu control.

```pascal
PROCEDURE RemoveEnhancedPullDownMenuItemRange(
				dialogID                : LONGINT;
				componentID             : LONGINT;
				iStartItemIndexToRemove : INTEGER;
				iEndItemIndexToRemove   : INTEGER);
```

```python
def vs.RemoveEnhancedPullDownMenuItemRange(dialogID, componentID, iStartItemIndexToRemove, iEndItemIndexToRemove):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|iStartItemIndexToRemove|INTEGER|   |
|iEndItemIndexToRemove|INTEGER|   |

## Examples
```pascal
RemoveEnhancedPullDownMenuItemRange(1, 2, 3, 10);
```
```python
import vs

# Removes the specified range of items from the specified Layout Manager
# enhanced pull down menu control.
dialogID = 1
componentID = 2
iStartItemIndexToRemove = 1
iEndItemIndexToRemove = 1

vs.RemoveEnhancedPullDownMenuItemRange(dialogID, componentID, iStartItemIndexToRemove, iEndItemIndexToRemove)
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
