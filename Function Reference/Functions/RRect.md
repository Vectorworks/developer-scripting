# RRect

## Description
Procedure RRect creates a rounded rectangle object in a VectorWorks document.

Corner definition is controlled by parameter Diam, which determines the &quot;roundness&quot; of the rectangle corners. The X and Y components of Diam correspond to the major and minor axes of an oval defining the rectangle corner.

```pascal
PROCEDURE RRect(
				p1X,p1Y     : REAL;
				p2X,p2Y     : REAL;
				DiamX,DiamY : REAL);
```

```python
def vs.RRect(p1, p2, Diam):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1|REAL|Top left coordinate of rectangle.|
|p2|REAL|Bottom right coordinate of rectangle.|
|Diam|REAL|X and Y diameters of corner.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
BEGIN
RRect(0, 0, 1, 1, 0.25, 0.25);
{ the same as: RRectangleN(0, 0, 1, 0, 1, 1, .25, .25); }
END;
RUN(Example);
```
==== Python ====
```python

```

## See Also
VS Functions:
[Rect](Rect.md) 
| [RRectangleN](RRectangleN.md) 
| [GetRRDiam](GetRRDiam.md)

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
