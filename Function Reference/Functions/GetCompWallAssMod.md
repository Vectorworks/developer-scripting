# GetCompWallAssMod

## Description
Gets the wall associated modification of a component in an object.

```pascal
FUNCTION GetCompWallAssMod(
				object                         : HANDLE;
				componentIndex                 : INTEGER;
				VAR wallAssociatedModification : INTEGER): BOOLEAN;
```

```python
def vs.GetCompWallAssMod(object, componentIndex):
    return (BOOLEAN, wallAssociatedModification)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|wallAssociatedModification|INTEGER|Returns the wall associated modification of the component.  0 - None 1 - Clip walls 2 - Clipped by walls|

## Examples
```pascal
resultOK := GetCompWallAssMod(object, 1, 2);
```
```python
import vs

# Gets the wall associated modification of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, wallAssociatedModification = vs.GetCompWallAssMod(object, componentIndex)
vs.Message('GetCompWallAssMod returned: ' + str((ok, wallAssociatedModification)))
```

## See Also
VS Functions:
[SetCompWallAssMod](SetCompWallAssMod.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
