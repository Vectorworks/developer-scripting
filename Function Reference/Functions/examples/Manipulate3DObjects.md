#### VectorScript

```pascal
PROCEDURE IncreaseExtr;
{This script increases extruded objects in the selection by a user requested value.}
{by Paolo, on the VectorScript bulletin board}
VAR
oggetto :HANDLE;
increaseValue :REAL;

FUNCTION Increase(h :HANDLE) :BOOLEAN;
VAR
height, width, depth :REAL;
xRot, yRot, zRot :REAL;
p0X, p0Y, p0Z :REAL;
p1X, p1Y, p1Z :REAL;
result, isMirroredXY :BOOLEAN;
BEGIN
{check if the obj is an extrusion}
if (GetType(h) = 24) THEN BEGIN
result := Get3DOrientation(h, xRot, yRot, zRot, isMirroredXY);
Get3DCntr(h, p0X, p0Y, p0Z);

SetRot3D(h, 0, 0, 0, 0, 0, 0);
{here depth = extrusion value}
Get3DInfo(h, height, width, depth);

{I increase the depth}
SET3DInfo(h, height, width, depth + increaseValue);

SET3DRot(h, xRot, yRot, zRot , 0,0,0);

Get3DCntr(h, p1X, p1Y, p1Z);

{move of the misplacement p0-p1}
Move3DObj(h, p0X-p1X, p0Y-p1Y, p0Z-p1Z);
Get3DCntr(h, p1X, p1Y, p1Z);
END;
increase := FALSE;
END;

BEGIN
{ask the value to increase}
increaseValue := RealDialog('Increase extrusions in the selection of this value','10');
{apply to the selected set of objects}
ForEachObjectInList(increase, 2, 0, oggetto);
END;
RUN(IncreaseExtr);
```

#### Python

```python
def Increase(h):
	# {check if the obj is an extrusion}
	vs.Message(increaseValue )
	if (vs.GetType(h) == 24):
		
		result, xRot, yRot, zRot, isMirroredXY = vs.Get3DOrientation(h)
		p0, p0Z = vs.Get3DCntr(h)

	
		vs.SetRot3D(h, 0, 0, 0, 0, 0, 0)
		# {here depth = extrusion value}
		height, width, depth = vs.Get3DInfo(h)

		# {I increase the depth}
		vs.Set3DInfo(h, height, width, depth + increaseValue)

		vs.Set3DRot(h, xRot, yRot, zRot , 0,0,0)

		p1, p1Z = vs.Get3DCntr(h)

		# {move of the misplacement p0-p1}
		vs.Move3DObj(h, p0[0]-p1[0], p0[1]-p1[1], p0Z-p1Z)
		p1, p1Z = vs.Get3DCntr(h)

	increase = False
	
def IncreaseExtr():
	# {This script increases extruded objects in the selection by a user requested value.}
	# {by Paolo, on the VectorScript bulletin board}
	# {ask the value to increase}
	global increaseValue 
	increaseValue = vs.RealDialog('Increase extrusions in the selection of this value','10')
	vs.Message(increaseValue )
	# {apply to the selected set of objects}
	vs.ForEachObjectInList(Increase, 2, 0, vs.FObject())

increaseValue = 0
IncreaseExtr()
```
