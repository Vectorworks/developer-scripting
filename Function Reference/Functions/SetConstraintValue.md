# SetConstraintValue

## Description
Sets the referenced dimensional constraint to a new value.

```pascal
PROCEDURE SetConstraintValue(
				constraint : HANDLE;
				value      : REAL);
```

```python
def vs.SetConstraintValue(constraint, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|constraint|HANDLE|Handle to constraint being modified.|
|value|REAL|New value for the constraint.|

## Examples
```pascal
SetConstraintValue(constraint, 1.0);
```
```python
import vs

# Sets the referenced dimensional constraint to a new value.
constraint = vs.FSActLayer()  # handle to the first selected object on the active layer
value = 1.0

vs.SetConstraintValue(constraint, value)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Parametric Constraints](../Categories/Parametric%20Constraints.md)
