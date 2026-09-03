# SetComponentClass

## Description
Sets the class of a component in an object.

```pascal
FUNCTION SetComponentClass(
				obj            : HANDLE;
				componentIndex : INTEGER;
				componentClass : LONGINT): BOOLEAN;
```

```python
def vs.SetComponentClass(obj, componentIndex, componentClass):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|componentClass|LONGINT|The class of the component.|

## Examples
```pascal
resultOK := SetComponentClass(obj, 1, 2);
```
```python
import vs

# Sets the class of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
componentClass = 1

ok = vs.SetComponentClass(obj, componentIndex, componentClass)
if ok:
    vs.Message('SetComponentClass succeeded')
else:
    vs.Message('SetComponentClass failed')
```

## See Also
VS Functions:
[GetComponentClass](GetComponentClass.md)

## Version
Availability: from VectorWorks 2008

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
