# SetComponentName

## Description
Sets the name of a component in an object.

```pascal
FUNCTION SetComponentName(
				obj            : HANDLE;
				componentIndex : INTEGER;
				componentName  : STRING): BOOLEAN;
```

```python
def vs.SetComponentName(obj, componentIndex, componentName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|componentName|STRING|The name of the component.|

## Examples
```pascal
resultOK := SetComponentName(obj, 1, 'Example');
```
```python
import vs

# Sets the name of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
componentName = 'Example'

ok = vs.SetComponentName(obj, componentIndex, componentName)
if ok:
    vs.Message('SetComponentName succeeded')
else:
    vs.Message('SetComponentName failed')
```

## See Also
VS Functions:
[GetComponentName](GetComponentName.md)

## Version
Availability: from VectorWorks 2008

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
