# CreatePullDownSearch

## Description
Creates a pulldown menu with a search bar at the top.<BR>
<BR>
The contents of the pulldown should be filtered as you type in the search bar.<BR>
<BR>

```pascal
PROCEDURE CreatePullDownSearch(
				nDialogID     : LONGINT;
				nComponentID  : LONGINT;
				nWidthInChars : INTEGER);
```

```python
def vs.CreatePullDownSearch(nDialogID, nComponentID, nWidthInChars):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nWidthInChars|INTEGER|   |

## Examples
```pascal
CreatePullDownSearch(1, 2, 3);
```
```python
import vs

# Creates a pulldown menu with a search bar at the top.
nDialogID = 1
nComponentID = 2
nWidthInChars = 3

vs.CreatePullDownSearch(nDialogID, nComponentID, nWidthInChars)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from Vectorworks 2020

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
