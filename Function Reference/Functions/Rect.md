# Rect

## Description
Procedure Rect creates a rectangle object in a VectorWorks document.

The procedure will accept coordinate definitions by either of two methods : coordinate values or distance angle values. Coordinate values are the absolute coordinate locations(in the documents' coordinate system) and are expressed as x and y values. 

Distance-angle values are expressed as a distance and angle from the current pen position. For Rect, two distance angle pairs are required to specify the top left and bottom right of the rectangle object.

```pascal
PROCEDURE Rect(
				p1x : REAL;
				p1y : REAL;
				p2x : REAL;
				p2y : REAL);
```

```python
def vs.Rect(p1x, p1y, p2x, p2y):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p1x|REAL|Top left X coordinate of rectangle.|
|p1y|REAL|Top left Y coordinate of rectangle.|
|p2x|REAL|Bottom right X coordinate of rectangle.|
|p2y|REAL|Bottom right Y coordinate of rectangle.|

## Remarks
*_c_* (2016.03.28): An example using distance-angle. Don't forget to use the pound notation (#):
<code lang="vs">
MoveTo(10m, 20m); { set pen position at x, y: 10m, 20m }
Rect(1m, #0, 2m, #90); 
{ draws from the current pen position 
an unrotated rectangle with width = 1m and height = 2m }
</code>

## Examples
[SelectandDelObjects](examples/SelectandDelObjects.md)

## See Also
VS Functions:
[RRect](RRect.md)

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
