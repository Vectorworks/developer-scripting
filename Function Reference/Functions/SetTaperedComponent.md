# SetTaperedComponent

## Description
Sets the tapered component of the object.

```pascal
PROCEDURE SetTaperedComponent(
				object         : HANDLE;
				componentIndex : INTEGER);
```

```python
def vs.SetTaperedComponent(object, componentIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a slab, Slab Style, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|

## Examples
```pascal
SetTaperedComponent(object, 1);
```
```python
import vs

# Sets the tapered component of the object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

vs.SetTaperedComponent(object, componentIndex)
```

## See Also
VS Functions:
[GetTaperedComponent](GetTaperedComponent.md)

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
