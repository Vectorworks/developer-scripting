# AddSurface

## Description
Creates a new surface object by combining the two referenced surface objects. If the combination is successful (if the objects overlap), it deletes the original surface objects and returns the handle of the resultant object.

```pascal
FUNCTION AddSurface(
				s1 : HANDLE;
				s2 : HANDLE): HANDLE;
```

```python
def vs.AddSurface(s1, s2):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|s1|HANDLE|Handle to object.|
|s2|HANDLE|Handle to object.|

## Examples
dSurface}}

## See Also
VS Functions:
[ClipSurface](ClipSurface.md)

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
