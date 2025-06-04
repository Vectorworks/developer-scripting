# AddHole

## Description
AddHole uses a holeTemplate to create a hole inside objectToGetHole.  Upon success, objectToGetHole is converted to polyline.   holeTemplate is unchanged.

```pascal
FUNCTION AddHole(
				VAR objectToGetHole : HANDLE;
				holeTemplate        : HANDLE): BOOLEAN;
```

```python
def vs.AddHole(objectToGetHole, holeTemplate):
    return (BOOLEAN, objectToGetHole)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectToGetHole|HANDLE|A 2D object to be cut by holeTemplate.|
|holeTemplate|HANDLE|A 2D object to cut a hole out of objectToGetHole.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE AddHoleExample;
VAR
h1, h2 :HANDLE;
BEGIN
CallTool(-204);
h1 := FSActLayer;
CallTool(-204);
h2 := FSActLayer;
IF AddHole(h1, h2) THEN SetFPat(h1, 3);
END;
RUN(AddHoleExample);
```
==== Python ====
```python
def AddHoleExample():
	vs.CallTool(-204)
	h1 = vs.FSActLayer()
	if(h1 != none):
		vs.CallTool(-204)
		h2 = vs.FSActLayer()
		if vs.AddHole(h1, h2):
			vs.SetFPat(h1, 3)
AddHoleExample()
```

## Version
Availability: from VectorWorks10.1

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
