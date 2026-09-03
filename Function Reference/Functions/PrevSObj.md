# PrevSObj

## Description
Function PrevSObj returns the previous selected object in the list preceding the referenced object.

```pascal
FUNCTION PrevSObj(h : HANDLE): HANDLE;
```

```python
def vs.PrevSObj(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Examples
```pascal
	BEGIN
	ApplyMarkerStyleToSEM;
	pluginH	:= NextSObj(pluginH);
	END;
pluginH := PrevSObj(origObj);
While (pluginH <> NIL) Do
	BEGIN
	ApplyMarkerStyleToSEM;
	pluginH	:= PrevSObj(pluginH);

BEGIN
	ClipSurface (plateH, cutoutH);
	plateH := PrevSObj (cutoutH);
	HRotate (cutoutH, x0, y0, theta);
END;

SetSelect (gShaftH);
Rect (gX0 + a, gY0 + pWrenchFlatsDepth/2, gX0 + a + pWrenchFlatsLength, gY0 + pShaftDia1/2 + b);
rectH := LNewObj;
ClipSurface (gShaftH, rectH);
gShaftH := PrevSObj (rectH);
DelObject (rectH);
```
```python
import vs

# Function PrevSObj returns the previous selected object in the list
# preceding the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.PrevSObj(h)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
Relative calls:
* [NextObj](NextObj.md) | [PrevObj](PrevObj.md)
* [FObject](FObject.md) | [LObject](LObject.md)
* [FSActLayer](FSActLayer.md) | [LSActLayer](LSActLayer.md)
* [FSObject](FSObject.md)  | [LActLayer](LActLayer.md)
* [NextDObj](NextDObj.md) | [PrevDObj](PrevDObj.md)
* [NextSObj](NextSObj.md) | [PrevSObj](PrevSObj.md)

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
