# DeleteConstraint

## Description
Removes a constraint from the referenced object in the document.

```pascal
PROCEDURE DeleteConstraint(
				obj        : HANDLE;
				constraint : HANDLE);
```

```python
def vs.DeleteConstraint(obj, constraint):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|constraint|HANDLE|Handle to constraint being deleted.|

## Examples
```pascal
DeleteConstraint(obj, constraint);
```
```python
import vs

# Removes a constraint from the referenced object in the document.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
constraint = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

vs.DeleteConstraint(obj, constraint)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Parametric Constraints](../Categories/Parametric%20Constraints.md)
