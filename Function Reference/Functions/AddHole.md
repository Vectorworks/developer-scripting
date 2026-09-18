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
#### VectorScript ####
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
#### Python ####
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

```pascal
	IF AddHole (objH1, objH2) THEN
		{DelObject(objH2);}
		SetFPat (objH2, 0)
END

IF (gettype(h) = 21) THEN BEGIN
	temp_b := getnumholes(h,holenum);
	IF (holenum > 0) THEN FOR i := 1 TO holenum DO BEGIN
		temp_b := gethole(h,i,hole_OF_interest);
		temp_b := addhole(new_out_poly_h,hole_OF_interest);
		END;

BEGIN
	RRect (-(a/2 - t), (b/2 - t), (a/2 - t), -(b/2 - t), 2*ri, 2*ri);
	h2 := LNewObj;
	IF AddHole(h1, h2) THEN DelObj (h2);
END;
```
```python
import vs

# AddHole uses a holeTemplate to create a hole inside objectToGetHole.
objectToGetHole = vs.FSActLayer()  # handle to the first selected object on the active layer
holeTemplate = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok, objectToGetHole = vs.AddHole(objectToGetHole, holeTemplate)
vs.Message('AddHole returned: ' + str((ok, objectToGetHole)))
```

## Version
Availability: from VectorWorks10.1

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
