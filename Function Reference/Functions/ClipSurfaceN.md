# ClipSurfaceN

## Description
Creates a new surface object by subtracting the intersection of surfaces s1 and s2 from s1.

```pascal
FUNCTION ClipSurfaceN(
				s1 : HANDLE;
				s2 : HANDLE): HANDLE;
```

```python
def vs.ClipSurfaceN(s1, s2):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|s1|HANDLE|Surface to be subtracted from|
|s2|HANDLE|Surface to subtract from s1|

## Remarks
[[User: CBMptr|ptr]]: (2022.05.09): This command deletes the s1 object but not the s2 object. 

[[User: CBM-c-| _c_]]: (2021.03.05):
This clips only parts that intersect the sides of the clipper, it doesn't clip inside the clipper, probably because it would mean deleting geometry.

Example:

[[File:vsClipSurfaceN.png]]

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
