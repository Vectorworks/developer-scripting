# GetSingularConstraint

## Description
Returns the type of constraint applied to the referenced object.

{| class="wikitable_c"
|+ Table - Constraint Types
! Index !! Constraint Type
|-
| style="text-align:center" | 4 
| Vertical 
|-
| style="text-align:center" | 5 
| Horizontal 
|-
| style="text-align:center" | 8 
| Distance 
|-
| style="text-align:center" | 9 
| Vertical distance 
|-
| style="text-align:center" | 10 
| Horizontal distance 
|-
| style="text-align:center" | 11 
| Radius
|}

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
