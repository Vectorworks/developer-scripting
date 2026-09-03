# SetComponentFunction

## Description
Sets the function of a component in an object.

```pascal
FUNCTION SetComponentFunction(
				object         : HANDLE;
				componentIndex : INTEGER;
				func           : INTEGER): BOOLEAN;
```

```python
def vs.SetComponentFunction(object, componentIndex, func):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|func|INTEGER|The function of the component.  0 - Other 1 - Load-Bearing 2 - Insulation 3 - Inner Finish 4 - Outer Finish 5 - Air Gap|

## Examples
```pascal
resultOK := SetComponentFunction(object, 1, 2);
```
```python
import vs

# Sets the function of a component in an object.
def handle_object(objHandle):
    vs.Message('Processing: ' + str(objHandle))

object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
func = handle_object

ok = vs.SetComponentFunction(object, componentIndex, func)
if ok:
    vs.Message('SetComponentFunction succeeded')
else:
    vs.Message('SetComponentFunction failed')
```

## See Also
VS Functions:
[GetComponentFunction](GetComponentFunction.md)

## Version
Availability: from Vectorworks 2018

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
