# IntersectSolid

## Description
Function IntersectSolid creates a new solid intersection object from the referenced source objects.

**Table - Solids Operation Result Codes**

| Operation Result     | Result Code |
|----------------------|-------------|
| Success              | 0           |
| Null geometry error  | 1           |
| Geometry error       | 2           |
| Out of memory error  | 4           |
| Bad group error      | 5           |
| Invalid object type  | 6           |
| Bad input            | 20          |

```pascal
FUNCTION IntersectSolid(
				obj1         : HANDLE;
				obj2         : HANDLE;
				VAR newSolid : HANDLE): INTEGER;
```

```python
def vs.IntersectSolid(obj1, obj2):
    return (INTEGER, newSolid)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj1|HANDLE|Handle to source object for intersect operation.|
|obj2|HANDLE|Handle to source object for intersect operation.|
|newSolid|HANDLE|Handle to resultant object from intersect operation.|

## Version
Availability: from MiniCAD 7.0

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
