# SetFillIAxisEndPoint

## Description
Sets the I-axis end point of the fill.

Note: only works with 2D objects that have a gradient or image fill.

```pascal
PROCEDURE SetFillIAxisEndPoint(
				objectHandle   : HANDLE;
				xIAxisEndPoint : REAL;
				yIAxisEndPoint : REAL);
```

```python
def vs.SetFillIAxisEndPoint(objectHandle, xIAxisEndPoint, yIAxisEndPoint):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to the object with fill.|
|xIAxisEndPoint|REAL|X coordinate of I-axis point.|
|yIAxisEndPoint|REAL|Y coordinate of I-axis point.|

## Examples
#### VectorScript ####
```pascal
SetFillIAxisEndPoint(objectHandle, 20.0, 10.0);
```
#### Python ####
```python

```

```pascal
SetFillIAxisEndPoint( ObjHand, ImageFillOriginVec.x + ImageFill_IAxisVec.x, ImageFillOriginVec.y + ImageFill_IAxisVec.y );
SetFillJAxisEndPoint( ObjHand, ImageFillOriginVec.x + ImageFill_JAxisVec.x, ImageFillOriginVec.y + ImageFill_JAxisVec.y );

SetFillOriginPoint( ObjHand, ImageFillOriginVec.x, ImageFillOriginVec.y );
SetFillIAxisEndPoint( ObjHand, ImageFillOriginVec.x + ImageFill_IAxisVec.x, ImageFillOriginVec.y + ImageFill_IAxisVec.y );
SetFillJAxisEndPoint( ObjHand, ImageFillOriginVec.x + ImageFill_JAxisVec.x, ImageFillOriginVec.y + ImageFill_JAxisVec.y );
```
```python
vs.SetFillIAxisEndPoint(h, (0, 0), (0, 0))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
