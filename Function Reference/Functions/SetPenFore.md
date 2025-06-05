# SetPenFore

## Description
Procedure SetPenFore sets the pen foreground color of the referenced object. RGB values are in the range of 0~65535.

```pascal
PROCEDURE SetPenFore(
				h     : HANDLE;
				color : LONGINT);
```

```python
def vs.SetPenFore(h, color):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|color|LONGINT|RGB color value.|

## Remarks
([[User:CBM-c-|_c_]] 2015.05.18): This Vectorscript routine responds to multiple types of notations:

Vectorscript:
* Singular [ color index](RGBToColorIndex.md):
*: <code>colorIndex := RGBToColorIndex(65535, 0, 0);</code>
*: <code>SetPenFore(FSActLayer, colorIndex);</code>
* Three RGB longints:
*: <code>SetPenFore(FSActLayer, 65535, 0, 0);</code>
 
Python:
* Singular color index:
*: <code>vs.SetPenFore(vs.FSActLayer(), vs.RGBToColorIndex(65535, 0, 0)) </code>
* Three longints in a tuple:
*: <code>vs.SetPenFore(vs.FSActLayer(), (65535, 0, 0)) </code>
* Three hex numbers in a tuple:
*: <code>vs.SetPenFore(vs.FSActLayer(), (0xFFFF, 0, 0)) </code>

On Vectorlab there is a list of all color routines accepting multiple variable type, see: [http://www.vectorlab.info/index.php?title=Index_pitfalls#Colors Color Index].
; Warning: SetPenBack, SetPenFore will remove the "ByClass" attribute of the FILL as well. Remember to parse for it and restore it.


(Joel Sciamma 2006.08.14): To have no pen drawn, use SetLW to set the line weight to zero.

## Examples
[SelectandDelObjects](examples/SelectandDelObjects.md)

## See Also
VS Functions:
[RGBToColorIndex](RGBToColorIndex.md) 
| [ColorIndexToRGB](ColorIndexToRGB.md)

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
