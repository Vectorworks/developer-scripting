#### VectorScript

```pascal
PROCEDURE Example;
VAR
red, green, blue, color :LONGINT;
criteria :STRING;
BEGIN
red := 65535;
green := 0;
blue := 0;
RGBToColorIndex(red, green, blue, color);
Rect(0, 0, 1, 1);
SetPenFore(LNewObj, color);
DSelectAll;
criteria := Concat('(INSYMBOL & INVIEWPORT & (PF=', color, '))');
SelectObj(criteria);
Message(criteria);
DeleteObjs;
END;
RUN(Example);
```

#### Python

```python
def Example():
	red = 65535
	green = 0
	blue = 0
	color = vs.RGBToColorIndex(red, green, blue)
	vs.Rect(0, 0, 1, 1)
	vs.SetPenFore(vs.LNewObj(), color)
	vs.DSelectAll()
	criteria = vs.Concat('(INSYMBOL & INVIEWPORT & (PF=', color, '))')
	vs.SelectObj(criteria)
	vs.Message(criteria)
	vs.DeleteObjs()
Example()
```
