# FPenFore

## Description
Procedure FPenFore returns the current pen foreground color of the document. RGB values are in the range of 0~65535.

```pascal
PROCEDURE FPenFore(
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.FPenFore():
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|red|LONGINT|Returns RGB color component value.|
|green|LONGINT|Returns RGB color component value.|
|blue|LONGINT|Returns RGB color component value.|

## Examples
```pascal
BEGIN
	fPenFore(R,G,B);
	thk := fPenSize;
END ELSE
BEGIN
	GetPenFore(gLine,R,G,B);

BEGIN
	FPenFore (R, G, B);
	SetPenFore (objectH, R, G, B);
END;

savePenPat := FPenPatN;
savePenSize := FPenSize;
FPenFore(saveR, saveG, saveB);
PenPatN(gLeaderType);
PenSize(gLeaderThickness);
GetPenFore(ActiveParmHand, r, g, b);
PenFore(r, g, b);
```
```python
import vs

# Procedure FPenFore returns the current pen foreground color of the document.
red, green, blue = vs.FPenFore()
vs.Message('FPenFore returned: ' + str((red, green, blue)))
```

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) 
| [ColorIndexToRGB](ColorIndexToRGB.md)

## Version
Availability: from All Versions

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
