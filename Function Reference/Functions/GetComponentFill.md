# GetComponentFill

## Description
Gets the fill of a component in an object.

```pascal
FUNCTION GetComponentFill(
				obj            : HANDLE;
				componentIndex : INTEGER;
				VAR fill       : LONGINT): BOOLEAN;
```

```python
def vs.GetComponentFill(obj, componentIndex):
    return (BOOLEAN, fill)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|fill|LONGINT|Returns the fill of the component.  Positive values for patterns, negative ref numbers for hatches.|

## Examples
```pascal
resultOK := GetComponentFill(obj, 1, 2);
```
```python
import vs

# Gets the fill of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, fill = vs.GetComponentFill(obj, componentIndex)
vs.Message('GetComponentFill returned: ' + str((ok, fill)))
```

## See Also
VS Functions:
[SetComponentFill](SetComponentFill.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
