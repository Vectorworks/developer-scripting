# GetMirrorEmpty2DComp

## Description
Gets whether the opposite view graphics are mirrored for empty 2D components of a symbol definition or plug-in object.

```pascal
FUNCTION GetMirrorEmpty2DComp(objectHandle : HANDLE): BOOLEAN;
```

```python
def vs.GetMirrorEmpty2DComp(objectHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle of a symbol or plug-in object.|

## Examples
```pascal
resultOK := GetMirrorEmpty2DComp(objectHandle);
```
```python
import vs

# Gets whether the opposite view graphics are mirrored for empty 2D
# components of a symbol definition or plug-in object.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetMirrorEmpty2DComp(objectHandle)
if ok:
    vs.Message('GetMirrorEmpty2DComp succeeded')
else:
    vs.Message('GetMirrorEmpty2DComp failed')
```

## See Also
VS Functions:
[SetMirrorEmpty2DComp](SetMirrorEmpty2DComp.md) 
| [Get2DComponentGroup](Get2DComponentGroup.md) 
| [Set2DComponentGroup](Set2DComponentGroup.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
