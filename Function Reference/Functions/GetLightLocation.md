# GetLightLocation

## Description
Procedure GetLightLocation returns the position of the referenced light object.

```pascal
PROCEDURE GetLightLocation(
				h            : HANDLE;
				VAR pX,pY,pZ : REAL);
```

```python
def vs.GetLightLocation(h):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to light.|
|p|REAL|Returns coordinate location of light.|

## Examples
```pascal
	BEGIN
Writeln(Concat('Light Hand:',h));
GetLightLocation(h,R1,R2,R3);
Writeln('Location:',R1,',',R2,',',R3);
GetLightInfo(h,I1,R1,B1,B2);
Writeln('Type:',I1,' Brightness:',I1,' On:',B1,' Shadow:',B2);
GetBeamAngle(h, R1);

GetLightLocation(LightObjHan,
							  gLightXLoc[SceneNumber, LightNum],
							  gLightYLoc[SceneNumber, LightNum],
							  gLightZLoc[SceneNumber, LightNum]
					);
IF IsPio THEN
	BEGIN
	TempHand := GetParent(LightObjHan);
	IF TempHand <> NIL THEN
```
```python
import vs

# Procedure GetLightLocation returns the position of the referenced light object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

result = vs.GetLightLocation(h)
```

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
