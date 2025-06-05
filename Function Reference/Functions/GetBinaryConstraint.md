# GetBinaryConstraint

## Description
Returns a handle to a binary parametric constraint applied to the referenced objects.

**Table - Binary Constraint Types**

| Index | Constraint Type      |
|-------|---------------------|
| 1     | coincident          |
| 2     | collinear           |
| 3     | parallel            |
| 6     | tangent             |
| 7     | concentric          |
| 8     | distance            |
| 9     | horizontal distance |
| 10    | vertical distance   |
| 12    | angle               |
| 13    | perpendicular       |

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
