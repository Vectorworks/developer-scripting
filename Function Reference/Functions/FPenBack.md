# FPenBack

## Description
Procedure FPenBack returns the current pen background color. RGB values are in the range of 0~65535.

```pascal
PROCEDURE FPenBack(
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.FPenBack():
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
cps := FPenSize;
FFillFore(rff,gff,bff);
FFillBack(rfb,gfb,bfb);
FPenFore(rpf,gpf,bpf);
FPenBack(rpb,gpb,bpb);

FPenFore( outPenFore[1], outPenFore[2], outPenFore[3] );
FPenBack( outPenBack[1], outPenBack[2], outPenBack[3] );
FFillFore( outFillFore[1], outFillFore[2], outFillFore[3] );
FFillBack( outFillBack[1], outFillBack[2], outFillBack[3] );
```
```python
import vs

# Procedure FPenBack returns the current pen background color.
red, green, blue = vs.FPenBack()
vs.Message('FPenBack returned: ' + str((red, green, blue)))
```

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) 
| [ColorIndexToRGB](ColorIndexToRGB.md)

## Version
Availability: from All Versions

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
