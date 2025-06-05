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

## Version
Availability: from VectorWorks 9.0

## Category
* [Parametric Constraints](../Categories/Parametric%20Constraints.md)
