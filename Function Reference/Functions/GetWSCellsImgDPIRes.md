# GetWSCellsImgDPIRes

## Description
Gets the DPI resolution for images in the specified worksheet.

```pascal
PROCEDURE GetWSCellsImgDPIRes(
				worksheet         : HANDLE;
				VAR dpiResolution : INTEGER);
```

```python
def vs.GetWSCellsImgDPIRes(worksheet):
    return dpiResolution
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|The worksheet handle.|
|dpiResolution|INTEGER|The images' DPI resolution|

## Examples
```pascal
GetWSCellsImgDPIRes(worksheet, 1);
```
```python
import vs

# Gets the DPI resolution for images in the specified worksheet.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet

result = vs.GetWSCellsImgDPIRes(worksheet)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Worksheets](../Categories/Worksheets.md)
