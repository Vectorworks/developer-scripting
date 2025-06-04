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

## See Also
VS Functions:
[SetComponentFill](SetComponentFill.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
