# SetProportionalBinding

## Description
Sets a dialog control?s bindings to be proportional.  Proportional bindings maintain a distance that is a ratio of the initial position to the width (or height, as appropriate) of the parent.  To change a control?s bindings to be fixed, use SetEdgeBinding.

```pascal
PROCEDURE SetProportionalBinding(
				dialogID           : LONGINT;
				itemID             : LONGINT;
				leftProportional   : BOOLEAN;
				rightProportional  : BOOLEAN;
				topProportional    : BOOLEAN;
				bottomProportional : BOOLEAN);
```

```python
def vs.SetProportionalBinding(dialogID, itemID, leftProportional, rightProportional, topProportional, bottomProportional):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |
|leftProportional|BOOLEAN|   |
|rightProportional|BOOLEAN|   |
|topProportional|BOOLEAN|   |
|bottomProportional|BOOLEAN|   |

## Examples
```pascal
SetEdgeBinding        (dialog1, kStaticText6,  TRUE, FALSE, FALSE, FALSE);
SetEdgeBinding        (dialog1, kPopup7,       TRUE, TRUE, FALSE, FALSE);
SetEdgeBinding        (dialog1, kStaticText8,  TRUE, FALSE, FALSE, FALSE);
SetEdgeBinding        (dialog1, kPopup9,       TRUE, TRUE, FALSE, FALSE);
SetProportionalBinding(dialog1, kImagePopup5,  FALSE, TRUE, FALSE, FALSE);
SetProportionalBinding(dialog1, kPopup7,       FALSE, TRUE, FALSE, FALSE);
SetProportionalBinding(dialog1, kPopup9,       FALSE, TRUE, FALSE, FALSE);

{set bindings}
SetEdgeBinding        ( dlgId, kSettingsPanel, TRUE, TRUE, FALSE, FALSE );
SetProportionalBinding( dlgId, kSettingsPanel, FALSE, TRUE, FALSE, FALSE );
SetEdgeBinding        ( dlgId, kHeightEdit, TRUE, TRUE, FALSE, FALSE );
SetEdgeBinding        ( dlgId, kFloorCountEdit, TRUE, TRUE, FALSE, FALSE );
SetEdgeBinding        ( dlgId, kSlabThicknessEdit, TRUE, TRUE, TRUE, TRUE );
SetEdgeBinding        ( dlgId, kLBSettingsPanel, TRUE, TRUE, TRUE, TRUE );

SetEdgeBinding(dialogID, 4, TRUE, True, True, True);
SetProportionalBinding(dialogID,4,FALSE, True, FALSE, FALSE);
SetEdgeBinding(dialogID, 14, TRUE, True, True, True);
SetProportionalBinding(dialogID,14,True, FALSE, FALSE, FALSE);
SetEdgeBinding(dialogID, 16, True, True, FALSE, True);
SetProportionalBinding(dialogID,16,True, FALSE, FALSE, FALSE);
```
```python
import vs

# s bindings to be proportional.
dialogID = 1
itemID = 2
leftProportional = True
rightProportional = True
topProportional = True
bottomProportional = True

vs.SetProportionalBinding(dialogID, itemID, leftProportional, rightProportional, topProportional, bottomProportional)
```

## See Also
VS Functions:
[CreateResizableLayout](CreateResizableLayout.md) 
| [SetEdgeBinding](SetEdgeBinding.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
