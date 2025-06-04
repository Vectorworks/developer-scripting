# SetBinaryConstraint

## Description
Applies a binary parametric constraint to the referenced objects. The geometry of the constraint is defined by the specified object vertices. 

{| class="wikitable_c"
|+ Table - Binary Constraint Types
! Index !! Constraint Type
|-
| style="text-align:center" | 1
| coincident
|-
| style="text-align:center" | 2
| collinear
|-
| style="text-align:center" | 3
| parallel 
|-
| style="text-align:center" | 6
| tangent 
|-
| style="text-align:center" | 7
| concentric
|-
| style="text-align:center" | 8
| distance 
|-
| style="text-align:center" | 9
| horizontal distance
|-
| style="text-align:center" | 10
| vertical distance
|-
| style="text-align:center" | 12
| angle
|-
| style="text-align:center" | 13
| perpendicular
|}

To apply a constraint to an object within a symbol, use [[VS:GetClosestPt| GetClosestPt]] to obtain an index to the object and pass the index to either obj2VertA to use it as the first object or obj2VertB to use it as the second object. In all other instances, pass 0 to both these parameters.

```pascal
FUNCTION SetBinaryConstraint(
				typeOfConstraint : INTEGER;
				h1               : HANDLE;
				h2               : HANDLE;
				obj1VertA        : INTEGER;
				obj1VertB        : INTEGER;
				obj2VertA        : INTEGER;
				obj2VertB        : INTEGER;
				containedObj1    : LONGINT;
				containedObj2    : LONGINT): BOOLEAN;
```

```python
def vs.SetBinaryConstraint(typeOfConstraint, h1, h2, obj1VertA, obj1VertB, obj2VertA, obj2VertB, containedObj1, containedObj2):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|typeOfConstraint|INTEGER|Type of constraint to be applied.|
|h1|HANDLE|Handle to object accepting constraint.|
|h2|HANDLE|Handle to object accepting constraint.|
|obj1VertA|INTEGER|Vertex on first object defining constraint geometry.|
|obj1VertB|INTEGER|Vertex on first object defining constraint geometry.|
|obj2VertA|INTEGER|Vertex on second object defining constraint geometry.|
|obj2VertB|INTEGER|Vertex on second object defining constraint geometry.|
|containedObj1|LONGINT|Object index, obtained from the GetClosestPt function.|
|containedObj2|LONGINT|Object index, obtained from the GetClosestPt function.|

## Remarks
Sets a constraint on h1 and h2 on the designated vertices.  Valid values for typeOfConstraint are 1 (coincident), 2 (collinear), 3 (parallel), 6 (tangent), 7 (concentric), 8 (distance), 9 (horizontal distance), 10 (vertical distance), 12 (angle) and 13 (perpendicular).  obj1VertA and obj1VertB indicate which vertices of the first object to use in the constraint, and obj2VertA and obj2VertB indicate which vertices of the second object to use.  A value of -1 indicates that a vertex parameter is not applicable. The containedObj fields are for an index into the list of a container object such as a symbol.  This can be obtained from the [[VS:GetClosestPt| GetClosestPt]] function.

## Version
Availability: from VectorWorks 9.0

## Category
* [Parametric Constraints](../Categories/Parametric%20Constraints.md)
