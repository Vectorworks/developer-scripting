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

## Examples
```pascal
SetWSImageScaleF(handle, 1.0, TRUE);
```
```python
import vs

# Sets the scale factor for the specified worksheet on drawing object.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
scaleFactor = 1.0
redraw = True

vs.SetWSImageScaleF(handle, scaleFactor, redraw)
```
See also in tutorials: [30. Publish Worksheet Image on a Sheet Layer](ai%20examples/30_WorksheetPublishOnSheet.md)

## Version
Availability: from Vectorworks 2017

## Category
* [Worksheets](../Categories/Worksheets.md)
