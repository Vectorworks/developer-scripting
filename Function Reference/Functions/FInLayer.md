# FInLayer

## Description
Function FInLayer returns a handle to the first object within the referenced layer. If the layer is empty, the function returns NIL.

```pascal
FUNCTION FInLayer(h : HANDLE): HANDLE;
```

```python
def vs.FInLayer(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to layer.|

## Examples
```pascal
BEGIN
ForEachObjectInList(FindDB,0,0,FInLayer(LHand));
GetShortSheet := TmpShortSheet;
END;

{ ----- look for any drawing label objects on the same layer as the border and update them ----- }
ForEachObjectInList (UpdateDrawingLabel, 0, 1, FInLayer (ActLayer));

BEGIN
hObj := FInLayer(hTempLayer);
While (hObj <> Nil) AND (Not Found) DO
				BEGIN
				IF GetClass(hObj) = ClassList(I) THEN Found := True;
				hObj := NextObj(hObj);
```
```python
import vs

# Function FInLayer returns a handle to the first object within the
# referenced layer.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.FInLayer(h)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
