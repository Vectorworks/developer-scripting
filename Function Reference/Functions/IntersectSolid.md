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

## Examples
```pascal
objH3 := createTeeth (outsideDia_1, rootDia_1, outsideDia_2, rootDia_2, depth, -pt [9].y, 0, numTeeth, 1);
result := IntersectSolid (objH2, objH3, objH2);
result := AddSolid (objH1, objH2, objH1);

	NoAngleVar;
EndXtrd;
objH1 := LNewObj;
SET3DRot (LNewObj, -90, 0, 0, 0, 0, 0);
status3D := IntersectSolid (objH1, objH2, objH1);
createHexBoltHead := objH1;

status3D := IntersectSolid (objH1, objH2, objH1);
createHexBoltHead := objH1;
```
```python
import vs

# Function IntersectSolid creates a new solid intersection object from the
# referenced source objects.
obj1 = vs.FSActLayer()  # handle to the first selected object on the active layer
obj2 = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

resultN, newSolid = vs.IntersectSolid(obj1, obj2)
vs.Message('IntersectSolid returned: ' + str((resultN, newSolid)))
```

## Version
Availability: from MiniCAD 7.0

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
