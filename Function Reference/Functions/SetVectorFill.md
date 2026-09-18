# SetVectorFill

## Description
Function SetVectorFill assigns the specified vector fill to the referenced object. The function returns TRUE if the operation was successful.

```pascal
FUNCTION SetVectorFill(
				theObj    : HANDLE;
				hatchName : STRING): BOOLEAN;
```

```python
def vs.SetVectorFill(theObj, hatchName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theObj|HANDLE|Handle to object.|
|hatchName|STRING|Name of vector fill to be assigned.|

## Remarks
Returns true if theObj was assigned the hatch specified by hatchName.

## Examples
```pascal
BEGIN
	  IF ( gVectorFillName <> '') THEN
		bResult := SetVectorFill(LNewObj, gVectorFillName);

BEGIN
	boolChoice := SetVectorFill(temp_h, JoistFillHatch);
END;

Absolute;
MoveTo (x - w1/2, y - (depth + hs));
Relative;
Rect (0, 0, w1, -h1);
IF SetVectorFill (LNewObj, hatchName) THEN
SetLW (LNewObj, 0);
```
```python
import vs

# Function SetVectorFill assigns the specified vector fill to the referenced
# object.
theObj = vs.FSActLayer()  # handle to the first selected object on the active layer
hatchName = 'Example'

ok = vs.SetVectorFill(theObj, hatchName)
if ok:
    vs.Message('SetVectorFill succeeded')
else:
    vs.Message('SetVectorFill failed')
```

## Version
Availability: from MiniCAD7.0.1

## Category
* [Hatches @ Vector Fills](../Categories/Hatches%20-%20Vector%20Fills.md)
