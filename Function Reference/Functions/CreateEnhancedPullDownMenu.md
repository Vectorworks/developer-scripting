# CreateEnhancedPullDownMenu

## Description
Creates a Layout Manager enhanced pull down menu control.

```pascal
PROCEDURE CreateEnhancedPullDownMenu(
				dialogID              : LONGINT;
				componentID           : LONGINT;
				iWidthInCharacters    : INTEGER;
				bShowIconInMainWindow : BOOLEAN);
```

```python
def vs.CreateEnhancedPullDownMenu(dialogID, componentID, iWidthInCharacters, bShowIconInMainWindow):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|iWidthInCharacters|INTEGER|   |
|bShowIconInMainWindow|BOOLEAN|   |

## Examples
```pascal
CreateEnhancedPullDownMenu(1, 2, 3, TRUE);
```
```python
import vs

# Creates a Layout Manager enhanced pull down menu control.
dialogID = 1
componentID = 2
iWidthInCharacters = 3
bShowIconInMainWindow = True

vs.CreateEnhancedPullDownMenu(dialogID, componentID, iWidthInCharacters, bShowIconInMainWindow)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
