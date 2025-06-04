# HCenter

## Description
Procedure HCenter returns the logical center point of the object specified in h. For most objects, this is the center of the bounding box. For circles, arcs, and round walls HCenter returns the arc center of the object.

```pascal
PROCEDURE HCenter(
				h         : HANDLE;
				VAR pX,pY : REAL);
```

```python
def vs.HCenter(h):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|p|REAL|X-Y location of object center.|

## Version
Availability: from All Versions

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
