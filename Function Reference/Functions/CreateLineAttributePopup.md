# CreateLineAttributePopup

## Description
Create a dialog control that displays both line style and line weight choices available in the current document.

```pascal
PROCEDURE CreateLineAttributePopup(
				dialogID : LONGINT;
				itemID   : LONGINT);
```

```python
def vs.CreateLineAttributePopup(dialogID, itemID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |

## Examples
```pascal
CreatePulldownMenu       (IDLabelDialog, kLabelShape,        16);
CreateCheckBoxGroupBox   (IDLabelDialog, kShowLeader,        GetStr(kShowLeader), TRUE);
CreateStaticText         (IDLabelDialog, kMarkerStyleTxt,      GetStr(kMarkerStyleTxt), 13);
CreateStaticText         (IDLabelDialog, kLineStyleTxt,      GetStr(kLineStyleTxt), 15);
CreateLineAttributePopup (IDLabelDialog, kIDLeaderLS);
CreateStaticText         (IDLabelDialog, kIDClassTxt,      GetStr(kIDClassTxt), 16);
CreateClassPullDownMenu  (IDLabelDialog, kLabelClass,        16);
CreateGroupBox			 (IDLabelDialog, kGroupBox7,		GetStr(KGroupBox7), FALSE);
CreateCheckBox			 (IDLabelDialog, kAutoRotate,   GetStr(kAutoRotateTxt));
```
```python
import vs

# Create a dialog control that displays both line style and line weight
# choices available in the current document.
dialogID = 1
itemID = 2

vs.CreateLineAttributePopup(dialogID, itemID)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
