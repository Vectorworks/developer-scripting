# GetColorButton

## Description
Gets the color of a modern dialog color button.

```pascal
PROCEDURE GetColorButton(
				dialogID  : LONGINT;
				itemID    : LONGINT;
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.GetColorButton(dialogID, itemID):
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index of the color button.|
|red|LONGINT|The red component of the color.|
|green|LONGINT|The green component of the color.|
|blue|LONGINT|The blue component of the color.|

## See Also
VS Functions:
[SetColorButton](SetColorButton.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
