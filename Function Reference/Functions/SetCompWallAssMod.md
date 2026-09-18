# SetCompWallAssMod

## Description
Sets the wall associated modification of a component in an object.

```pascal
FUNCTION SetCompWallAssMod(
				object                     : HANDLE;
				componentIndex             : INTEGER;
				wallAssociatedModification : INTEGER): BOOLEAN;
```

```python
def vs.SetCompWallAssMod(object, componentIndex, wallAssociatedModification):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|wallAssociatedModification|INTEGER|The wall associated modification of the component.  0 - None 1 - Clip walls 2 - Clipped by walls|

## Examples
```pascal
resultOK := SetCompWallAssMod(object, 1, 2);
```
```python
import vs

# Sets the wall associated modification of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
wallAssociatedModification = 1

ok = vs.SetCompWallAssMod(object, componentIndex, wallAssociatedModification)
if ok:
    vs.Message('SetCompWallAssMod succeeded')
else:
    vs.Message('SetCompWallAssMod failed')
```

## See Also
VS Functions:
[GetCompWallAssMod](GetCompWallAssMod.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
