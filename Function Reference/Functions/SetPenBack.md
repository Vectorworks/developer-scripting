# SetPenBack

## Description
Procedure SetPenBack sets the pen background color of the referenced object. RGB values are in the range of 0~65535.

```pascal
PROCEDURE SetPenBack(
				h     : HANDLE;
				color : LONGINT);
```

```python
def vs.SetPenBack(h, color):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|color|LONGINT|RGB color value.|

## Remarks
(\_c\_ 2015.05.18): This Vectorscript routine responds to multiple types of notations:

Vectorscript:
* Singular [ color index](RGBToColorIndex.md):
*: <code>colorIndex := RGBToColorIndex(65535, 0, 0);</code>
*: <code>SetPenBack(FSActLayer, colorIndex);</code>
* Three RGB longints:
*: <code>SetPenBack(FSActLayer, 65535, 0, 0);</code>
 
Python:
* Singular color index:
*: <code>vs.SetPenBack(vs.FSActLayer(), vs.RGBToColorIndex(65535, 0, 0)) </code>
* Three longints in a tuple:
*: <code>vs.SetPenBack(vs.FSActLayer(), (65535, 0, 0)) </code>
* Three hex numbers in a tuple:
*: <code>vs.SetPenBack(vs.FSActLayer(), (0xFFFF, 0, 0)) </code>

On Vectorlab there is a list of all color routines accepting multiple variable type, see: [http://www.vectorlab.info/index.php?title=Index_pitfalls#Colors Color Index].
; Warning: SetPenBack, SetPenFore will remove the "ByClass" attribute of the FILL as well. Remember to parse for it and restore it.

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) 
| [ColorIndexToRGB](ColorIndexToRGB.md)

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
