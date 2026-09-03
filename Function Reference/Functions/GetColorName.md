# GetColorName

## Description
Retrieves the color name of the specified color index.

```pascal
FUNCTION GetColorName(ColorIndex : INTEGER): STRING;
```

```python
def vs.GetColorName(ColorIndex):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ColorIndex|INTEGER|The index of the color|

## Examples
```pascal
	green:=65535;
	blue:=65535;
END;
RGBToColorIndexN(red, blue, green, gelIndex, TRUE);
IF GetColorName(gelIndex) <> colorList[i].colorSort THEN BEGIN
	boo:=SetColorName(gelIndex, colorList[i].colorSort);
END;
```
```python
import vs

# Retrieves the color name of the specified color index.
ColorIndex = 1

name = vs.GetColorName(ColorIndex)
vs.Message('GetColorName returned: ' + str(name))
```

## See Also
VS Functions:
[SetColorName](SetColorName.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Object Names](../Categories/Object%20Names.md)
