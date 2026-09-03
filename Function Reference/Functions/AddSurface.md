# AddSurface

## Description
Creates a new surface object by combining the two referenced surface objects. If the combination is successful (if the objects overlap), it deletes the original surface objects and returns the handle of the resultant object.

```pascal
FUNCTION AddSurface(
				s1 : HANDLE;
				s2 : HANDLE): HANDLE;
```

```python
def vs.AddSurface(s1, s2):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|s1|HANDLE|Handle to object.|
|s2|HANDLE|Handle to object.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE AddSurfaceExample;
VAR
	h1, h2, h3 :HANDLE;
BEGIN
	DSelectAll;
	CallTool(-203);
	h1 := FSActLayer;
	DSelectAll;
	CallTool(-203);
	h2 := FSActLayer;
	h3 := AddSurface(h1, h2);
	IF h3 <> nil THEN SetFPat(h3, 5);
END;
RUN(AddSurfaceExample);
```

#### Python ####
The python code will not pause for the execution of CallTool, that's why it uses a callback mechanism for the script to know when the temp tool has finished.

```python
# this will not be called prior Vectorworks 2022 SP3
# as the calback functions will not be executed prior to that version
def Example():
	vs.DSelectAll()

	def resultCallback1():
		h1 = vs.FSActLayer()
		vs.DSelectAll()
		
		def resultCallback2():
			h2 = vs.FSActLayer()
			h3 = vs.AddSurface(h1, h2)
			if h3 != None :  
				vs.SetFPat(h3, 5)
		
		
		vs.CallTool(-203, resultCallback2)
			
	vs.CallTool(-203, resultCallback1)

Example()
```

```pascal
done := TRUE;
for cnt1 := 1 to wall_cnt do BEGIN
	for cnt2 := (cnt1 + 1) to wall_cnt do BEGIN
		if cnt2 <= wall_cnt then BEGIN
			temp_h := AddSurface(walls[cnt1], walls[cnt2]);
			if temp_h <> nil then BEGIN
				walls[cnt1] := temp_h;
				for cnt3 := cnt2 to wall_cnt DO walls[cnt3] := walls[cnt3+1];
				wall_cnt := wall_cnt - 1;

Oval(-.5 * Scale, .375 * Scale, .5 * Scale, .125 * Scale);
h1 := LNewObj;
Rect(-.5 * Scale, .25 * Scale, .5 * Scale, -.25 * Scale);
h2 := LNewObj;
h1 := AddSurface(h1, h2);
Oval(-.5 * Scale, -.125 * Scale, .5 * Scale, -.375 * Scale);
h2 := LNewObj;
h1 := AddSurface(h1, h2);
Oval(-.5 * Scale, .375 * Scale, .5 * Scale, .125 * Scale);

Rect (-f*x [1], 0, f*x[1], f*f1*y [2]);
h2 := LNewObj;
h1 := AddSurface (h1, h2);
```
```python
import vs

# Creates a new surface object by combining the two referenced surface objects.
s1 = vs.FSActLayer()  # handle to the first selected object on the active layer
s2 = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

objHandle = vs.AddSurface(s1, s2)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
VS Functions:
[ClipSurface](ClipSurface.md)

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
