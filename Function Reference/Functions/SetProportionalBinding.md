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

## See Also
VS Functions:
[CreateResizableLayout](CreateResizableLayout.md) 
| [SetEdgeBinding](SetEdgeBinding.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
