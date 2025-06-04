# SetWSImageScaleF

## Description
Sets the scale factor for the specified worksheet on drawing object.

```pascal
PROCEDURE SetWSImageScaleF(
				handle      : HANDLE;
				scaleFactor : REAL;
				redraw      : BOOLEAN);
```

```python
def vs.SetWSImageScaleF(handle, scaleFactor, redraw):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|The handle to the worksheet on drawing object.|
|scaleFactor|REAL|The scale factor.|
|redraw|BOOLEAN|Indicates whether to immediately redraw the worksheet on drawing.|

## Version
Availability: from Vectorworks 2017

## Category
* [Worksheets](../Categories/Worksheets.md)
