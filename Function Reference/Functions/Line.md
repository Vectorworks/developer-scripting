# Line

## Description
Procedure Line creates a line object in VectorWorks. The line is drawn from the current pen position(x,y) to the specified point. The point may also be thought of as the location (x+dX,y+dY), where dX and dY are x and y offsets, respectively. 

The line object is drawn with the current default attributes unless otherwise specified.

```pascal
PROCEDURE Line(line : REAL);
```

```python
def vs.Line(line):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|line|REAL|Offset values for line.|

## Examples
#### VectorScript ####
```pascal
Line(2,2);
{ draws a line from the current pen location to a point }
{ 2 horizontal and 2 vertical units away.               }
```
#### Python ####
```python

```

```pascal
BEGIN
	Line (0, tickMark [3]);
	SetLW (LNewObj, markerPenSize);
	Move (dx, -tickMark [3]);
END

BEGIN
	MoveTo(0, theWidth/2);
	Line(0, -theWidth);
END;

IF pstyle = kSUStyleOpen THEN BEGIN
	ChangeToClass( gBracketClass );
	BeginXtrd(0",pheight);
		offset:=0;
		Moveto(0,0-thick);Line(0,thick);Line(thick,0);
		IF pconfig = kSUConfigRightCorner THEN BEGIN { right corner shelf unit }
			Moveto(0,-wdth+thick);
			Line(0,-thick);
			Line(thick,0);
```
```python
vs.Line(line)
```
See also in tutorials: [02. Draw 2D Geometry Primitives](ai%20examples/02_Draw2DPrimitives.md)

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
