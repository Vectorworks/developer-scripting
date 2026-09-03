# SetWllHoleObjIgnClsr

## Description
Sets whether an object in the 3D Wall Hole group of a plug-in object ignores wall closures.

```pascal
PROCEDURE SetWllHoleObjIgnClsr(
				object        : HANDLE;
				ignoreClosure : BOOLEAN);
```

```python
def vs.SetWllHoleObjIgnClsr(object, ignoreClosure):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object in the 3D Wall Hole group of a plug-in object|
|ignoreClosure|BOOLEAN|Whether the object ignores wall closures.|

## Examples
```pascal
SetWllHoleObjIgnClsr(object, TRUE);
```
```python
import vs

# Sets whether an object in the 3D Wall Hole group of a plug-in object
# ignores wall closures.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
ignoreClosure = True

vs.SetWllHoleObjIgnClsr(object, ignoreClosure)
```

## See Also
VS Functions:
[GetWllHoleObjIgnClsr](GetWllHoleObjIgnClsr.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
