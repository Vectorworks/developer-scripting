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

## Version
Availability: from Vectorworks 2011

## Category
* [Object Info](../Categories/Object%20Info.md)
