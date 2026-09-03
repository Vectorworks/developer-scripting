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

## Examples
```pascal
resultH := GetBinaryConstraint(1, obj1, obj2, 2, 3, 10, 5, 1, 2);
```
```python
import vs

# Returns a handle to a binary parametric constraint applied to the
# referenced objects.
constrType = 0
obj1 = vs.FSActLayer()  # handle to the first selected object on the active layer
obj2 = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
obj1VertA = 1
obj1VertB = 2
obj2VertA = 3
obj2VertB = 10
containedObj1 = 1
containedObj2 = 2

objHandle = vs.GetBinaryConstraint(constrType, obj1, obj2, obj1VertA, obj1VertB, obj2VertA, obj2VertB, containedObj1, containedObj2)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks 9.0

## Category
* [Parametric Constraints](../Categories/Parametric%20Constraints.md)
