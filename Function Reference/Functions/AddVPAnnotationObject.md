# AddVPAnnotationObject

## Description
Adds the specified annotation object to the specified viewport.

```pascal
FUNCTION AddVPAnnotationObject(
				viewportHandle   : HANDLE;
				annotationHandle : HANDLE): BOOLEAN;
```

```python
def vs.AddVPAnnotationObject(viewportHandle, annotationHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|   |
|annotationHandle|HANDLE|   |

## Examples
```pascal
resultOK := AddVPAnnotationObject(viewportHandle, annotationHandle);
```
```python
import vs

# Adds the specified annotation object to the specified viewport.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
annotationHandle = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok = vs.AddVPAnnotationObject(viewportHandle, annotationHandle)
if ok:
    vs.Message('AddVPAnnotationObject succeeded')
else:
    vs.Message('AddVPAnnotationObject failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
