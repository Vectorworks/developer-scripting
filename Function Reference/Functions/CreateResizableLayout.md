# CreateResizableLayout

## Description
Creates a new resizable Layout Manager dialog.

Resizable dialogs raise the ResizeDialogC event when resized.

```pascal
FUNCTION CreateResizableLayout(
				dialogTitle       : STRING;
				hasHelp           : BOOLEAN;
				defaultButtonName : STRING;
				cancelButtonName  : STRING;
				widthResizable    : BOOLEAN;
				heightResizable   : BOOLEAN): LONGINT;
```

```python
def vs.CreateResizableLayout(dialogTitle, hasHelp, defaultButtonName, cancelButtonName, widthResizable, heightResizable):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogTitle|STRING|   |
|hasHelp|BOOLEAN|   |
|defaultButtonName|STRING|   |
|cancelButtonName|STRING|   |
|widthResizable|BOOLEAN|   |
|heightResizable|BOOLEAN|   |

## Remarks
The parameters are the same as CreateLayout, except for widthResizable and heightResizable, which specify that the width and height, respectively, be resizable.  A dialog ID is returned by the function.

## See Also
VS Functions:
[SetEdgeBinding](SetEdgeBinding.md) 
| [SetProportionalBinding](SetProportionalBinding.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
