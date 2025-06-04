# RectangleN

## Description
Creates and returns a handle to a new rectangle object with the specified bounds.

```pascal
PROCEDURE RectangleN(
				orginX,orginY         : REAL;
				directionX,directionY : REAL;
				width                 : REAL;
				height                : REAL);
```

```python
def vs.RectangleN(orgin, direction, width, height):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|orgin|REAL|   |
|direction|REAL|   |
|width|REAL|   |
|height|REAL|   |

## Remarks
This procedure does not return a handle.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
BEGIN
RectangleN(0, 0, 1, 0, 1, 1);
END;
RUN(Example);
```
==== Python ====
```python
origin = [0, 1]
direction = [10, 10]
width = 5
height = 2

vs.RectangleN ( origin[0], origin[1], direction[0], direction[1], width, height )
```

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
