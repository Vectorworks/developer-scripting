# ShowEnhancedPullDownMenuGroupIcon

## Description
Determines if the group icon should be shown in the specified enhanced pull down menu.

```pascal
PROCEDURE ShowEnhancedPullDownMenuGroupIcon(
				liDialogID     : LONGINT;
				liComponentID  : LONGINT;
				bShowGroupIcon : BOOLEAN);
```

```python
def vs.ShowEnhancedPullDownMenuGroupIcon(liDialogID, liComponentID, bShowGroupIcon):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|liDialogID|LONGINT|   |
|liComponentID|LONGINT|   |
|bShowGroupIcon|BOOLEAN|   |

## Examples
```pascal
ShowEnhancedPullDownMenuGroupIcon(1, 2, TRUE);
```
```python
import vs

# Determines if the group icon should be shown in the specified enhanced pull
# down menu.
liDialogID = 1
liComponentID = 2
bShowGroupIcon = True

vs.ShowEnhancedPullDownMenuGroupIcon(liDialogID, liComponentID, bShowGroupIcon)
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
