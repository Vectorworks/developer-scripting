# FFillFore

## Description
Procedure FFillFore returns the current fill foreground color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE FFillFore(
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.FFillFore():
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|red|LONGINT|Returns RGB color component value.|
|green|LONGINT|Returns RGB color component value.|
|blue|LONGINT|Returns RGB color component value.|

## Examples
#### VectorScript ####
```pascal
FFillFore(redValue,greenValue,blueValue);
```
#### Python ####
```python
redValue,greenValue,blueValue = vs.FFillFore()
```

```pascal
BEGIN
	FFillFore (R, G, B);
	SetFillFore (objectH, R, G, B);
	FFillBack (R, G, B);
	SetFillBack (objectH, R, G, B);
END;

FFillFore (red, green, blue);
RGBToColorIndex (red, green, blue, color);
TmpClassInfo.FillFore := color;

{get attributes}
cpp := FPenPatN;
cfp := FFillPat;
cps := FPenSize;
FFillFore(rff,gff,bff);
FFillBack(rfb,gfb,bfb);
FPenFore(rpf,gpf,bpf);
FPenBack(rpb,gpb,bpb);
```
```python
import vs

# Procedure FFillFore returns the current fill foreground color.
red, green, blue = vs.FFillFore()
vs.Message('FFillFore returned: ' + str((red, green, blue)))
```

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) 
| [ColorIndexToRGB](ColorIndexToRGB.md)

## Version
Availability: from All Versions

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
