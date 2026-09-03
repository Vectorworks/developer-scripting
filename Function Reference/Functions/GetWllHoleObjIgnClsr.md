# GetWllHoleObjIgnClsr

## Description
Gets whether an object in the 3D Wall Hole group of a plug-in object ignores wall closures.

```pascal
FUNCTION GetWllHoleObjIgnClsr(object : HANDLE): BOOLEAN;
```

```python
def vs.GetWllHoleObjIgnClsr(object):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object in the 3D Wall Hole group of a plug-in object|

## Examples
```pascal
resultOK := GetWllHoleObjIgnClsr(object);
```
```python
import vs

# Gets whether an object in the 3D Wall Hole group of a plug-in object
# ignores wall closures.
object = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetWllHoleObjIgnClsr(object)
if ok:
    vs.Message('GetWllHoleObjIgnClsr succeeded')
else:
    vs.Message('GetWllHoleObjIgnClsr failed')
```

## See Also
VS Functions:
[SetWllHoleObjIgnClsr](SetWllHoleObjIgnClsr.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
