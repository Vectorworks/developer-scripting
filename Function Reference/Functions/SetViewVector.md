# SetViewVector

## Description
Sets the view direction of the active document.

```pascal
PROCEDURE SetViewVector(
				locationX,locationY,locationZ : REAL;
				targetX,targetY,targetZ       : REAL;
				upX,upY,upZ                   : REAL);
```

```python
def vs.SetViewVector(location, target, up):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|location|REAL|3D coordinate of view origin.|
|target|REAL|3D coordinate of view target.|
|up|REAL|3D coordinate indicating camera up direction.|

## Version
Availability: from VectorWorks9.0

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
