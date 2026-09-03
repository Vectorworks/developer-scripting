# SetMirrorEmpty2DComp

## Description
Sets whether the opposite view graphics are mirrored for empty 2D components of a symbol definition or plug-in object.

```pascal
FUNCTION SetMirrorEmpty2DComp(
				objectHandle : HANDLE;
				doMirror     : BOOLEAN): BOOLEAN;
```

```python
def vs.SetMirrorEmpty2DComp(objectHandle, doMirror):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle of a symbol or plug-in object.|
|doMirror|BOOLEAN|Whether the opposite view graphics are mirrored for empty 2D components.|

## Examples
```pascal
resultOK := SetMirrorEmpty2DComp(objectHandle, TRUE);
```
```python
import vs

# Sets whether the opposite view graphics are mirrored for empty 2D
# components of a symbol definition or plug-in object.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
doMirror = True

ok = vs.SetMirrorEmpty2DComp(objectHandle, doMirror)
if ok:
    vs.Message('SetMirrorEmpty2DComp succeeded')
else:
    vs.Message('SetMirrorEmpty2DComp failed')
```

## See Also
VS Functions:
[GetMirrorEmpty2DComp](GetMirrorEmpty2DComp.md) 
| [Get2DComponentGroup](Get2DComponentGroup.md) 
| [Set2DComponentGroup](Set2DComponentGroup.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
