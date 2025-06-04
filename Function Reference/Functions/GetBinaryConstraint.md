# GetBinaryConstraint

## Description
Returns a handle to a binary parametric constraint applied to the referenced objects.

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

```pascal
FUNCTION GetBinaryConstraint(
				constrType    : INTEGER;
				obj1          : HANDLE;
				obj2          : HANDLE;
				obj1VertA     : INTEGER;
				obj1VertB     : INTEGER;
				obj2VertA     : INTEGER;
				obj2VertB     : INTEGER;
				containedObj1 : LONGINT;
				containedObj2 : LONGINT): HANDLE;
```

```python
def vs.GetBinaryConstraint(constrType, obj1, obj2, obj1VertA, obj1VertB, obj2VertA, obj2VertB, containedObj1, containedObj2):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|constrType|INTEGER|Type of constraint to be returned.|
|obj1|HANDLE|Handle to first object in constraint relationship.|
|obj2|HANDLE|Handle to second object in constraint relationship.|
|obj1VertA|INTEGER|Vertex defining the constraint geometry of first object.|
|obj1VertB|INTEGER|Vertex defining the constraint geometry of first object.|
|obj2VertA|INTEGER|Vertex defining the constraint geometry of second object.|
|obj2VertB|INTEGER|Vertex defining the constraint geometry of second object.|
|containedObj1|LONGINT|   |
|containedObj2|LONGINT|   |

## Version
Availability: from VectorWorks 9.0

## Category
* [Parametric Constraints](../Categories/Parametric%20Constraints.md)
