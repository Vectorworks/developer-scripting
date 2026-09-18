# SetWSImgShowDBHeader

## Description
Set worksheet image to either show or hide database headers. Also provides choice of whether to redraw the worksheet image.

```pascal
PROCEDURE SetWSImgShowDBHeader(
				hWorksheetImage : HANDLE;
				show            : BOOLEAN;
				redrawImage     : BOOLEAN);
```

```python
def vs.SetWSImgShowDBHeader(hWorksheetImage, show, redrawImage):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hWorksheetImage|HANDLE|   |
|show|BOOLEAN|   |
|redrawImage|BOOLEAN|   |

## Examples
```pascal
SetWSImgShowDBHeader(hWorksheetImage, TRUE, FALSE);
```
```python
import vs

# Set worksheet image to either show or hide database headers.
hWorksheetImage = vs.GetObject('MyWorksheet')  # handle to a worksheet
show = True
redrawImage = True

vs.SetWSImgShowDBHeader(hWorksheetImage, show, redrawImage)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Worksheets](../Categories/Worksheets.md)
