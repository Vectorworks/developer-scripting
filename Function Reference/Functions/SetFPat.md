# SetFPat

## Description
Procedure SetFPat sets the fill pattern of the referenced object.

To apply a bitmap fill pattern, use positive value corresponding to the index  of the bitmap pattern.  To apply a vector fill pattern, use the negative of the vector fill index (index * -1).

Fill patterns and their associated constants can be found in the [VectorScript Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#fill-patterns).

```pascal
PROCEDURE SetFPat(
				h           : HANDLE;
				fillPattern : LONGINT);
```

```python
def vs.SetFPat(h, fillPattern):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|fillPattern|LONGINT|Fill index value.|

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

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
