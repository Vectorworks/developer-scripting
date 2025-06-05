#### VectorScript

```pascal
PROCEDURE Example;
VAR
x1, y1, x2, y2 :REAL;
resourceID :LONGINT;
h : HANDLE;
BEGIN
SetWallWidth(3.5");
GetPt(x1, y1);
GetPtL(x1, y1, x2, y2);
MoveTo(x1, y1);
WallTo(x2, y2);
h := LActLayer;
AddSymToWall(h,3',0',FALSE,FALSE,'Door-1');
AddWallBottomPeak(h,24'0",2'6");
END;
RUN(Example);
```

#### Python

```python
def MyWallto(pt):
	vs.WallTo(pt[0], pt[1])
def MyMoveto(pt):
	vs.MoveTo(pt[0], pt[1])
def Example():
	vs.SetWallWidth(3.5)
	vs.GetPt( MyMoveto )
	vs.GetPt( MyWallto )	
	h = vs.LActLayer()
	vs.AddSymToWall(h,3,0,False,False,'Door-1')
	vs.AddWallBottomPeak(h,24*12+0,2*12+6)
Example()
```
