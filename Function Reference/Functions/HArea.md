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

## Version
HArea is obsolete as of VectorWorks 12.5


Availability: from All Versions

## Category
* [Object Info](../Categories/Object%20Info.md)
