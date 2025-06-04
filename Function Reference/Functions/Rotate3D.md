# Rotate3D

## Description
Procedure Rotate3D rotates the most recently created three-dimensional object. Rotation values are applied about the respective axes.

```pascal
PROCEDURE Rotate3D(
				xAngle : REAL;
				yAngle : REAL;
				zAngle : REAL);
```

```python
def vs.Rotate3D(xAngle, yAngle, zAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|xAngle|REAL|Rotation about X-axis.|
|yAngle|REAL|Rotation about Y-axis|
|zAngle|REAL|Rotation about Z-axis.|

## Remarks
From Julian:
Rotate3D() can only be called after object creation. Duplication does not count as a newly created object, so use Set3DRot() instead. If you are rotating in more than one axis, you may need to use it 3 times, first Z, then Y then X rotation.

## Examples
#### VectorScript ####
```pascal
BeginXtrd(0&quot;,4&quot;);
Rect(0&quot;,3&quot;,1&quot;,0&quot;);
EndXtrd;
Rotate3D(21d 10' 22&quot;,-18d 44' 50&quot;,-7d 5' 45&quot;);
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [General Edit](../Categories/General%20Edit.md)
