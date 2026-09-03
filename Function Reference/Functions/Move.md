# Move

## Description
Sets the position of the graphics pen in the VectorWorks document by moving a specified distance from the current pen location.

Horizontal and vertical offsets from the initial location. The final position of the pen at a point whose coordinates are (x+moveDX, y+moveDY).

```pascal
PROCEDURE Move(move : REAL);
```

```python
def vs.Move(move):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|move|REAL|X-Y offset distance.|

## Remarks
The difference between this and MoveTo is that this is relative, whereas MoveTo is absolute.

## Examples
#### VectorScript ####
```pascal
Move(6,1);
{ moves the graphics pen 6 units to the right }
{ and 1 unit up from the current position.    }
```
#### Python ####
```python
vs.Move(6, 1)
```

```pascal
BEGIN
	Line (0, tickMark [3]);
	SetLW (LNewObj, markerPenSize);
	Move (dx, -tickMark [3]);
END

	Move (-(dx2 + dx1), height - dy3);
	PenLoc (x, y);
	numLines := numLines + 1;
END;

begin
Move((sWidth + gAisleWidth)/2, #0);
PenLoc(center_x, center_y);
end else begin
Move((sWidth - gAisleWidth)/2, #0);
PenLoc(center_x, center_y);
```
```python
import vs

# Sets the position of the graphics pen in the VectorWorks document by moving
# a specified distance from the current pen location.
move = 1.0

vs.Move(move)
```

## See Also
VS Functions:
[MoveTo](MoveTo.md)

## Version
Availability: from All Versions

## Category
* [Command](../Categories/Command.md)
