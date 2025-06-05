# BuildConstraintModelForObject

## Description
Create a constraint model for the specified object in the constraint manager. If 'traverseContainers' is true and the specified object is a symbol definition, a group or another container-like objects, it will go deep inside that container.<BR>
This function should typically be called for constrained objects that have been duplicated and newly inserted into the drawing.

```pascal
PROCEDURE BuildConstraintModelForObject(
				h                  : HANDLE;
				traverseContainers : BOOLEAN);
```

```python
def vs.BuildConstraintModelForObject(h, traverseContainers):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object|
|traverseContainers|BOOLEAN|Whether to traverse containers-like objects|

## Examples
[TraverseObjectsInActiveLayer](examples/TraverseObjectsInActiveLayer.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Parametric Constraints](../Categories/Parametric%20Constraints.md)
