# SetCompWallAssBound

## Description
Sets the wall associated bound of a component in an object.

```pascal
FUNCTION SetCompWallAssBound(
				object              : HANDLE;
				componentIndex      : INTEGER;
				wallAssociatedBound : INTEGER): BOOLEAN;
```

```python
def vs.SetCompWallAssBound(object, componentIndex, wallAssociatedBound):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|wallAssociatedBound|INTEGER|The wall associated bound of the component.  0 - Inner face 1 - Outer face of inner component 2 - Inner face of core 3 - Center of core 4 - Outer face of core 5 - Inner face of outer component 6 - Roof edge 7 - Roof axis line|

## Examples
```pascal
resultOK := SetCompWallAssBound(object, 1, 2);
```
```python
import vs

# Sets the wall associated bound of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
wallAssociatedBound = 1

ok = vs.SetCompWallAssBound(object, componentIndex, wallAssociatedBound)
if ok:
    vs.Message('SetCompWallAssBound succeeded')
else:
    vs.Message('SetCompWallAssBound failed')
```

## See Also
VS Functions:
[GetCompWallAssBound](GetCompWallAssBound.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
