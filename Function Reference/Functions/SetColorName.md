# SetColorName

## Description
Sets the color name of the specified color index.

```pascal
FUNCTION SetColorName(
				ColorIndex : INTEGER;
				ColorName  : STRING): BOOLEAN;
```

```python
def vs.SetColorName(ColorIndex, ColorName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ColorIndex|INTEGER|The index of the color to be named.|
|ColorName|STRING|The new name of the color specified by the index.|

## Examples
```pascal
BEGIN
	bFlipTexture := SetColorName (ColorChoiceNdx,NewColorNameString);
	bNameChanged := FALSE;
END;

	blue:=65535;
END;
RGBToColorIndexN(red, blue, green, gelIndex, TRUE);
IF GetColorName(gelIndex) <> colorList[i].colorSort THEN BEGIN
	boo:=SetColorName(gelIndex, colorList[i].colorSort);
END;
```
```python
import vs

# Sets the color name of the specified color index.
ColorIndex = 1
ColorName = 'Example'

ok = vs.SetColorName(ColorIndex, ColorName)
if ok:
    vs.Message('SetColorName succeeded')
else:
    vs.Message('SetColorName failed')
```

## See Also
VS Functions:
[GetColorName](GetColorName.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Object Names](../Categories/Object%20Names.md)
