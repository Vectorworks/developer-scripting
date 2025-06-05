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


## See Also
VS Functions:
[ClipSurface](ClipSurface.md)

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
