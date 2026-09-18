# ConsolidatePlanar

## Description
Modifies the plane of the second planar object so it is on the plane of the first object. Also moves the object so plane change doesn't affect it's position.

```pascal
FUNCTION ConsolidatePlanar(
				obj1 : HANDLE;
				obj2 : HANDLE): BOOLEAN;
```

```python
def vs.ConsolidatePlanar(obj1, obj2):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj1|HANDLE|Handle to the first object.|
|obj2|HANDLE|Handle to the second object.|

## Examples
```pascal
resultOK := ConsolidatePlanar(obj1, obj2);
```
```python
import vs

# Modifies the plane of the second planar object so it is on the plane of the
# first object.
obj1 = vs.FSActLayer()  # handle to the first selected object on the active layer
obj2 = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok = vs.ConsolidatePlanar(obj1, obj2)
if ok:
    vs.Message('ConsolidatePlanar succeeded')
else:
    vs.Message('ConsolidatePlanar failed')
```

## Version
Availability: from Vectorworks 2011

## Category
* [Object Info](../Categories/Object%20Info.md)
