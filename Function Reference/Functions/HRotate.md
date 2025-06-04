# HRotate

## Description
Procedure HRotate rotates the referenced object about a coordinate point location. rotationAngle is in degrees.

```pascal
PROCEDURE HRotate(
				h               : HANDLE;
				centerX,centerY : REAL;
				rotationAngle   : REAL);
```

```python
def vs.HRotate(h, center, rotationAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|center|REAL|X-Y coordinates of center point of rotation.|
|rotationAngle|REAL|Angle of rotation.|

## Examples
#### VectorScript ####
```pascal
HRotate(objHd,3,5,60d);
```
#### Python ####
```python
def Example():
	vs.HRotate(vs.FSActLayer(),3,5,60)

Example()
```

## Version
Availability: from MiniCAD6.0

## Category
* [Object Editing](../Categories/Object%20Editing.md)
