# WallFootPrint

## Description
Returns the handle of a polyline representing the footprint of a wall.

```pascal
FUNCTION WallFootPrint(wallHandle : HANDLE): HANDLE;
```

```python
def vs.WallFootPrint(wallHandle):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wallHandle|HANDLE|Handle to the wall|

## Remarks
[[User:CBM-c-|_c_]], (2008.01.07): This actually generates the footprint object in the parent container (active layer or whatever other parent). It doesn't only return a handle.

[[User:CBM-c-|_c_]], (2011.01.30): You might need to regen it using [[VS:ResetObject| ResetObject]] in order to actually see/use it in the drawing. Mind that this object is always a screen plane polyline, unregarded the active plane, and that its vertexes are all hidden.

## Examples
#### VectorScript ####
```pascal
PROCEDURE GetWallFootPrint;
VAR
h1, h2 :HANDLE;
BEGIN
h1 := FSActLayer;
h2 := WallFootPrint(h1);
END;
RUN(GetWallFootPrint);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks 10.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
