# SetColorButton

## Description
Sets the color of a modern dialog color button. Set all colors to 0 for black. Set all colors to 65535 for white.

```pascal
PROCEDURE SetColorButton(
				dialogID : LONGINT;
				itemID   : LONGINT;
				red      : LONGINT;
				green    : LONGINT;
				blue     : LONGINT);
```

```python
def vs.SetColorButton(dialogID, itemID, red, green, blue):
    return None
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
#### VectorScript ####
```pascal
PROCEDURE SetColorControl(dialogID, controlID :LONGINT; colorIndex :STRING);
VAR
r, g, b :LONGINT;
BEGIN
IF colorIndex <> '' THEN BEGIN
ColorIndexToRGB(Str2Num(colorIndex), r, g, b);
SetColorButton(dialogID, controlID, r, g, b);
END;
END;
```
#### Python ####
```python

```

```pascal
	SetBooleanItem(dialog1, 10,gDrawProposed);
	END;
checkBox12 := gDrawStation;
SetBooleanItem(dialog1, 12,gDrawStation);	{Draw Selected Station Profile}
SetColorButton(dialog1, 7,GridColor.red,GridColor.green,GridColor.blue);
SetColorButton(dialog1, 9,ExistingColor.red,ExistingColor.green,ExistingColor.blue);
SetColorButton(dialog1,11,ProposedColor.red,ProposedColor.green,ProposedColor.blue);
SetColorButton(dialog1,13,StakeColor.red,StakeColor.green,StakeColor.blue);

RGBToColorIndex(r, g, b, idx);
ColorIndexToRGB(idx, r, g, b);
SetColorButton(dlogID,itemID,r,g,b);
```
```python
vs.SetColorButton(dialogID, itemID, red, green, blue)
```

## See Also
VS Functions:
[GetColorButton](GetColorButton.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
