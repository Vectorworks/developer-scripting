# EnableLBUpdates

## Description
Determines if updates should be enabled for the specified list browser.

```pascal
PROCEDURE EnableLBUpdates(
				liDialogID     : LONGINT;
				liComponentID  : LONGINT;
				bEnableUpdates : BOOLEAN);
```

```python
def vs.EnableLBUpdates(liDialogID, liComponentID, bEnableUpdates):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|liDialogID|LONGINT|   |
|liComponentID|LONGINT|   |
|bEnableUpdates|BOOLEAN|   |

## Examples
```pascal
EnableLBUpdates(1, 2, TRUE);
```
```python
import vs

# Determines if updates should be enabled for the specified list browser.
liDialogID = 1
liComponentID = 2
bEnableUpdates = True

vs.EnableLBUpdates(liDialogID, liComponentID, bEnableUpdates)
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
