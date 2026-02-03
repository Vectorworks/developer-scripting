# CallTool

## Description
Activates the specified VectorWorks tool for a single use. After the tool has been used VectorWorks will revert back to the previously active tool.

Note: Please refer to the  [Script Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#settool---calltool-selectors) for specific tool ID values.

```pascal
PROCEDURE CallTool(toolID : INTEGER);
```

```python
def vs.CallTool(toolID, callback):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|toolID|INTEGER|VectorWorks tool constant.|
|callback|FUNCTION|Python only! A callback function that will be executed when the tool finishes.|

## Remarks
(Vlado, 2022.01.22): The python function requires an extra 'callback' parameter because python will not pause in the function, while the tool executes. The python will continue until the end of the script, and then the tool will be activated. The 'callback' function will be executed when the tool completes.
```python
vs.CallTool( -221, any ) # 'Any' is and does absolutely nothing in Vectorworks prior to 2022 SP3
```

(Tom): Changes the active tool to that specified by toolID. Waits until the user has executed the functionality of that tool, then switches back to the previously active tool &amp; returns.

I found that if you have a plug-in that uses the CallTool procedure to create an object (specifically a freehand poly) while you are in a group or editing a symbol definition, you cannot get the handle to the poly using the standard functions LNewObj, LSActLayer, LObject or any other I can think of.

I think I found a foolproof (?) solution:

1. Create a dummy object and get its handle (dummyH.)
2. Implement the CallTool procedure and create the poly.
3. Use "polyH := NextObj (dummyH)" to get the handle to the poly.
4. Delete the dummy object.

This works in nested groups as well as groups within symbols. If anyone knows of a simpler solution, please let me know.

(CLC 2001/06/24):  Another method is to do a DSelectAll at the beginning of the program, and then you should be able to find the last created entity by searching for selected items (ForEachObject(MyProcedure, (SEL=TRUE))), assuming that the object created by the tool is still selected. Depending on what you're doing, this may be simpler, but it's certainly a bit scarier.

(KGM 2002/5/21): If the user drops the tool then no object will be created and NextObj(DummyObj) will be NIL.

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


#### VectorScript ####
```pascal
PushAttrs;
PenFore(16);
PenBack(0);
PenPat(-2);
CallTool(-201);
PopAttrs;
```
#### Python ####
The python code will not pause for the execution of CallTool, that's why it uses a callback mechanism for the script to know when the temp tool has finished.
```python
vs.PushAttrs()
vs.PenFore(16)
vs.PenBack(0)
vs.PenPat(-2)

# this will not be called prior Vectorworks 2022 SP3
def finishedCallback():
	vs.PopAttrs()
	
vs.CallTool(-201, finishedCallback)
```

## See Also
VS Functions:
* [CallToolByIndex](CallToolByIndex.md)
* [CallToolByName](CallToolByName.md)

## Version
Availability: from MiniCAD 4.0

## Category
* [User Interactive](../Categories/User%20Interactive.md)
