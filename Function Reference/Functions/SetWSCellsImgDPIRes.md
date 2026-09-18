# SetWSCellsImgDPIRes

## Description
Sets the DPI resolution for images in the specified worksheet.

```pascal
PROCEDURE SetWSCellsImgDPIRes(
				worksheet     : HANDLE;
				dpiResolution : INTEGER);
```

```python
def vs.SetWSCellsImgDPIRes(worksheet, dpiResolution):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|The worksheet handle.|
|dpiResolution|INTEGER|The images' DPI resolution.|

## Examples
```pascal
SetWSCellsImgDPIRes(worksheet, 1);
```
```python
import vs

# Sets the DPI resolution for images in the specified worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
dpiResolution = 1

vs.SetWSCellsImgDPIRes(worksheet, dpiResolution)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Worksheets](../Categories/Worksheets.md)
