# FSActLayer

## Description
Function FSActLayer returns a handle to the first selected object on the active layer. If no objects are selected, the function returns NIL.

```pascal
FUNCTION FSActLayer : HANDLE;
```

```python
def vs.FSActLayer():
    return HANDLE
```

## Examples
```pascal
resultH := FSActLayer;
```
```python
import vs

# Function FSActLayer returns a handle to the first selected object on the
# active layer.
objHandle = vs.FSActLayer()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```
See also in tutorials: [20. Read a Polyline and Build Walls Along Its Path](ai%20examples/20_PolylineToWalls.md)

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
