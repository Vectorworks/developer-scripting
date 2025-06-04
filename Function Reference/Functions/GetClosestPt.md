# GetClosestPt

## Description
Returns the index number of the object closest to the specified location.  

The index value will return 0 if no vertex can be determined as closest, and will return -1 if the object does not support GetClosestPt.

For container objects, GetClosestPt has distinct behaviors. For walls, if the closest vertex is
is in a subobject, obj will be set to a handle to the subobject. For symbols and plug-in objects, an index to the sub-object will be returned via parameter containedObj.

GetClosestPt supports only 2D objects.

```pascal
PROCEDURE GetClosestPt(
				VAR obj          : HANDLE;
				ptX,ptY          : REAL;
				VAR index        : INTEGER;
				VAR containedObj : LONGINT);
```

```python
def vs.GetClosestPt(obj, pt):
    return (obj, index, containedObj)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|pt|REAL|Coordinate location of comparison point.|
|index|INTEGER|Index to vertex.|
|containedObj|LONGINT|Index of sub-object.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE GetClosestPtExample;
VAR
obj :HANDLE; 
ptX, ptY :REAL; 
index :INTEGER; 
containedObj :LONGINT;
BEGIN
GetPt(ptX, ptY);
obj := PickObject(ptX, ptY);
GetClosestPt(obj, ptX, ptY, index, containedObj);
SetPenFore(obj, 65535, 0, 0);
END;
RUN(GetClosestPtExample);
```
==== Python ====
```python
def PickPointCallback(pt):
	obj = vs.PickObject(pt[0], pt[1])	
	red = 65535
	green = 0
	blue = 0
	color = vs.RGBToColorIndex(red, green, blue)
	obj, index, containedObj = vs.GetClosestPt(obj, pt[0], pt[1])
	vs.SetPenFore(obj, color )

def GetClosestPtExample():
	vs.GetPt(PickPointCallback)	

GetClosestPtExample()
```

## Version
Availability: from VectorWorks8.5

## Category
* [Utility](../Categories/Utility.md)
