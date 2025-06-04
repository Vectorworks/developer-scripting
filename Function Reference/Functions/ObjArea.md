# ObjArea

## Description
Function ObjArea returns the area of the referenced object.

```pascal
FUNCTION ObjArea(h : HANDLE): REAL;
```

```python
def vs.ObjArea(h):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
([[User:Orso.b.schmid|Orso]], 2011 Jan. 27): ObjArea is affected by the application preference "2D Conversion Resolution" (PrefInt 55): the function will output faulty values on polylines with curved vertexes, if this preference is set to anything but "Very high" (512). It is advisable to set this preferences to 512 before using ObjArea and restore the user value at end of script. (tested VW 2010 and 2011).

## Version
Availability: from VectorWorks 12.5

## Category
* [Object Info](../Categories/Object%20Info.md)
