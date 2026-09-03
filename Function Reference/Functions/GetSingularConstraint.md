# GetSingularConstraint

## Description
Returns the type of constraint applied to the referenced object.

**Table - Constraint Types**

| Index | Constraint Type      |
|-------|---------------------|
| 4     | Vertical            |
| 5     | Horizontal          |
| 8     | Distance            |
| 9     | Vertical distance   |
| 10    | Horizontal distance |
| 11    | Radius              |

```pascal
FUNCTION GetSingularConstraint(
				typeOfConstraint : INTEGER;
				obj              : HANDLE;
				vertexA          : INTEGER;
				vertexB          : INTEGER): HANDLE;
```

```python
def vs.GetSingularConstraint(typeOfConstraint, obj, vertexA, vertexB):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|typeOfConstraint|INTEGER|Type of constraint to be returned.|
|obj|HANDLE|Handle to object.|
|vertexA|INTEGER|Vertex defining the constraint geometry.|
|vertexB|INTEGER|Vertex defining the constraint geometry.|

## Examples
```pascal
resultH := GetSingularConstraint(1, obj, 2, 3);
```
```python
import vs

# Returns the type of constraint applied to the referenced object.
typeOfConstraint = 0
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
vertexA = 1
vertexB = 2

objHandle = vs.GetSingularConstraint(typeOfConstraint, obj, vertexA, vertexB)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks 9.0

## Category
* [Parametric Constraints](../Categories/Parametric%20Constraints.md)
