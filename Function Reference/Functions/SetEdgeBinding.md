# SetEdgeBinding

## Description
Binds edges of a dialog control to its parent.  This function sets bindings to be fixed.  To change any of them to be proportional, use SetProportionalBinding.

```pascal
PROCEDURE SetEdgeBinding(
				dialogID      : LONGINT;
				itemID        : LONGINT;
				boundToLeft   : BOOLEAN;
				boundToRight  : BOOLEAN;
				boundToTop    : BOOLEAN;
				boundToBottom : BOOLEAN);
```

```python
def vs.SetEdgeBinding(dialogID, itemID, boundToLeft, boundToRight, boundToTop, boundToBottom):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |
|boundToLeft|BOOLEAN|   |
|boundToRight|BOOLEAN|   |
|boundToTop|BOOLEAN|   |
|boundToBottom|BOOLEAN|   |

## Remarks
Binding to an edge indicates that the control will maintain a predictable distance from one of its sides to the corresponding side of its parent.  Bindings can be either fixed or proportional.  Fixed bindings maintain a constant distance from their parent.  Proportional bindings maintain a distance that is a ratio of the initial position to the width (or height, as appropriate) of the parent.

## See Also
VS Functions:
[CreateResizableLayout](CreateResizableLayout.md) 
| [SetProportionalBinding](SetProportionalBinding.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
