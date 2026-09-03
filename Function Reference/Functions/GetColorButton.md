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

## Examples
```pascal
GetColorButton(dialogID, controlID, r1, g1, b1);

GetColorButton(dialog1, 7,GridColor.red,GridColor.green,GridColor.blue);
GetColorButton(dialog1, 9,ExistingColor.red,ExistingColor.green,ExistingColor.blue);
GetColorButton(dialog1,11,ProposedColor.red,ProposedColor.green,ProposedColor.blue);
GetColorButton(dialog1,13,StakeColor.red,StakeColor.green,StakeColor.blue);

BEGIN
	GetColorButton(dlogID,itemID,r,g,b);
```
```python
import vs

# Gets the color of a modern dialog color button.
dialogID = 1
itemID = 2

red, green, blue = vs.GetColorButton(dialogID, itemID)
vs.Message('GetColorButton returned: ' + str((red, green, blue)))
```

## See Also
VS Functions:
[SetColorButton](SetColorButton.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
