# HArea

## Description
_See [ObjArea](ObjArea.md) for a replacement function._
Function HArea returns the area of the referenced object.

```pascal
FUNCTION HArea(h : HANDLE): REAL;
```

```python
def vs.HArea(h):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
(*\_c\_*, 2011.01.27): HArea is affected by the application preference "2D Conversion Resolution" (PrefInt 55): will output faulty values on polylines with curved vertexes, if this preference is set to anything but "Very high" (512). It is advisable to set this preferences to 512 before using HArea and restore the user value at end of script. (tested VW 2010 and 2011).

(*\_c\_*, 2010.04.13): Replaced by [ ObjArea](ObjArea.md). ''HArea'' still works, but will always use the current settings for length primary units, while ''ObjArea'' will use the settings for Area units, which might be different. See preference flags 176-179 in the SDK.

## Examples
```pascal
{* Otherwise, check to see that the object does not have zero area *}
ELSE IF HArea (objH) = 0 THEN
BEGIN
	SysBeep;
	AlrtDialog (GetPlugInString (6002));
	isValidObject := FALSE;
END;

{
message (' x1 = ',x1,'  y1 = ',y1,'    xc = ',xc,'  yc = ',yc);
}
	{ get the other properties }
	area   := HArea(objH);
	perim  := HPerim(objH);
	height := HHeight(objH);
	width  := HWidth(objH);

BEGIN
	IF use_area
	THEN SetObjectVariableReal(pio_h,801,harea(poly_h))
	ELSE	IF zero_area
			THEN SetObjectVariableReal(pio_h,801,0.0);
	IF use_perim
	THEN SetObjectVariableReal(pio_h,802,hperim(poly_h))
	ELSE	IF zero_perim
			THEN SetObjectVariableReal(pio_h,802,0.0);
```
```python
import vs

# _ Function HArea returns the area of the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

area = vs.HArea(h)
vs.Message('HArea returned: ' + str(area))
```

## Version
HArea is obsolete as of VectorWorks 12.5

Availability: from All Versions

## Category
* [Object Info](../Categories/Object%20Info.md)
