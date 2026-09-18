# FSObject

## Description
Function FSObject returns the handle to the first selected object in the referenced layer. If no objects are selected, the function returns NIL.

```pascal
FUNCTION FSObject(h : HANDLE): HANDLE;
```

```python
def vs.FSObject(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to layer.|

## Examples
```pascal
BEGIN
pluginH := FSObject(currLayer);
while (pluginH <> NIL) Do
	BEGIN
	IF (pluginH <> origObj) THEN
		ApplyMarkerStyleToSEM;

{ go trough the selection. }
hSelObj 	:= FSObject( hLayer );

BEGIN
	TheMulti := FSObject(TheLayer);
	IF (GetName(GetParametricRecord(TheMulti)) = kBOLabelName) THEN
		BEGIN
			Obj := TheMulti;
			TheMulti := GetObject(GetRField(Obj,kBOLabelName,'MultiUID'));
```
```python
import vs

# Function FSObject returns the handle to the first selected object in the
# referenced layer.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.FSObject(h)
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
