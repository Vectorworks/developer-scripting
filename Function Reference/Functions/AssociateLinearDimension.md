# AssociateLinearDimension

## Description
Associates a linear dimension with an object when the dimension's endpoints are coincident with objects in the drawing.  When selectedObjectsMode is true, only selected objects will be checked to see if they should be associated with the linear dimension.

```pascal
PROCEDURE AssociateLinearDimension(
				h                   : HANDLE;
				selectedObjectsMode : BOOLEAN);
```

```python
def vs.AssociateLinearDimension(h, selectedObjectsMode):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|selectedObjectsMode|BOOLEAN|   |

## Version
Availability: from VectorWorks12.5

## Category
* [Dimensions](../Categories/Dimensions.md)
