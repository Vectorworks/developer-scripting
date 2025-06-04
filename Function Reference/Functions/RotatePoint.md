# RotatePoint

## Description
Procedure RotatePoint rotates selected VectorWorks objects about the specified coordinate point.

```pascal
PROCEDURE RotatePoint(
				pX,pY         : REAL;
				rotationAngle : REAL);
```

```python
def vs.RotatePoint(p, rotationAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Point of rotation.|
|rotationAngle|REAL|Rotation angle.|

## Examples
#### VectorScript ####
```pascal
SetSelect(LNewObj);
RotatePoint(0,3,45d);
```
#### Python ####
```python

```

## Version
Availability: from MiniCAD6.0

## Category
* [General Edit](../Categories/General%20Edit.md)
