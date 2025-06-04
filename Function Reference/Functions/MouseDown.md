# MouseDown

## Description
Return TRUE if a mouse down event has occurred within the active document window.

```pascal
FUNCTION MouseDown(VAR pX,pY : REAL): BOOLEAN;
```

```python
def vs.MouseDown():
    return (bool, (px, py))
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Coordinates of mouse click.|Remark for VW2014 python: Always an empty tuple (0, 0) - use GetMouse() if down == True|

## Remarks
This function returns a 2-dimensional point on the screen plane.

## Examples
#### VectorScript ####
```pascal
REPEAT
UNTIL MouseDown(x1,y1);
REPEAT
UNTIL MouseDown(x2,y2);
MoveTo(x1,y1);
LineTo(x2,y2);
```
#### Python ####
```python
down = False
while not down:
    down, pt = vs.MouseDown()  # pt is a tuple (x, y)

vs.AlrtDialog(str(pt))
```

## Version
Availability: from All Versions

## Category
* [User Interactive](../Categories/User%20Interactive.md)
