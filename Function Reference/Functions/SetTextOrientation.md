# SetTextOrientation

## Description
Procedure SetTextOrientation sets the position and orientation attributes of the referenced text object.

```pascal
PROCEDURE SetTextOrientation(
				theText                 : HANDLE;
				textOriginX,textOriginY : REAL;
				textAngle               : REAL;
				textIsMirrored          : BOOLEAN);
```

```python
def vs.SetTextOrientation(theText, textOrigin, textAngle, textIsMirrored):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|
|textOrigin|REAL|Coordinates of text object origin.|
|textAngle|REAL|Rotation angle for text object.|
|textIsMirrored|BOOLEAN|Mirroring setting for text object.|

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
