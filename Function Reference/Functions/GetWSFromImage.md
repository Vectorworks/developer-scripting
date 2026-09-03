# GetWSFromImage

## Description
Returns a handle to the worksheet being displayed by a worksheet image object..

```pascal
FUNCTION GetWSFromImage(worksheetImage : HANDLE): HANDLE;
```

```python
def vs.GetWSFromImage(worksheetImage):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheetImage|HANDLE|Handle to worksheet image object.|

## Examples
```pascal
resultH := GetWSFromImage(worksheetImage);
```
```python
import vs

# Returns a handle to the worksheet being displayed by a worksheet image object.
worksheetImage = vs.GetObject('MyWorksheet')  # handle to a worksheet

objHandle = vs.GetWSFromImage(worksheetImage)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
