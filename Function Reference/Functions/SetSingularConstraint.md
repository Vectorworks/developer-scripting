# SetSingularConstraint

## Description
Applies a parametric constraint to the referenced object. The geometry of the constraint is defined by the specified object vertices. 

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
FUNCTION SetSingularConstraint(
				typeOfConstraint : INTEGER;
				h                : HANDLE;
				vertexA          : INTEGER;
				vertexB          : INTEGER): BOOLEAN;
```

```python
def vs.SetSingularConstraint(typeOfConstraint, h, vertexA, vertexB):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|typeOfConstraint|INTEGER|Type of constraint to be applied.|
|h|HANDLE|Handle to object accepting constraint.|
|vertexA|INTEGER|Vertex defining the constraint geometry.|
|vertexB|INTEGER|Vertex defining the constraint geometry.|

## Remarks
Sets a constraint of type typeOfConstraint on the object h.  The valid values for typeOfConstraint are  4 (vertical), 5 (horizontal), 8 (distance), 9 (vertical distance), 10 (horizontal distance) and 11 (radius).  vertexA and vertexB indicate which vertices of the object define the geometry to be constrained.  A value of -1 indicates that a vertex parameter is not applicable.  It returns false if the constraint cannot be set.

## Version
Availability: from VectorWorks 9.0

## Category
* [Parametric Constraints](../Categories/Parametric%20Constraints.md)
