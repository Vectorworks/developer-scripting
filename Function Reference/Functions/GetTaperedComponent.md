# GetTaperedComponent

## Description
Gets the tapered component of the object.

```pascal
FUNCTION GetTaperedComponent(object : HANDLE): INTEGER;
```

```python
def vs.GetTaperedComponent(object):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a slab, Slab Style, or the Slab Preferences.|

## Examples
```pascal
resultN := GetTaperedComponent(object);
```
```python
import vs

# Gets the tapered component of the object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetTaperedComponent(object)
vs.Message('GetTaperedComponent returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetTaperedComponent](SetTaperedComponent.md)

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
