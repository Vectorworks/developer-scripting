# VPHasCropObject

## Description
Indicates if specified viewport has a crop object.

```pascal
FUNCTION VPHasCropObject(viewportHandle : HANDLE): BOOLEAN;
```

```python
def vs.VPHasCropObject(viewportHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|Handle to viewport.|

## Examples
```pascal
resultOK := VPHasCropObject(viewportHandle);
```
```python
import vs

# Indicates if specified viewport has a crop object.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.VPHasCropObject(viewportHandle)
if ok:
    vs.Message('VPHasCropObject succeeded')
else:
    vs.Message('VPHasCropObject failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
